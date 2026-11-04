# Arquitetura Técnica e Guia de Manutenção

Este documento detalha o funcionamento interno da aplicação **Olho Vivo • Grupo Performance Ocupacional** para facilitar futuras manutenções, customizações e implantações.

---

## 1. Visão Geral da Arquitetura

O aplicativo adota uma arquitetura **Single-File Web Application (`index.html`)**, sem dependências externas de *frameworks*, compiladores ou bancos de dados:

- **Zero dependências externas:** logotipo institucional embutido em `data:image/png;base64` e ilustrações geradas integralmente via **SVG vetorial paramétrico** em JavaScript.
- **Execução 100% offline-ready:** funciona tanto hospedado em servidores HTTPS (GitHub Pages, Intranet, Nginx/Apache) quanto aberto diretamente como arquivo local (`file://`) em celulares, tablets ou totens sem internet.
- **Leveza e carregamento instantâneo:** cerca de `124 KB` totais (HTML + CSS + logotipo + motor de 9 cenários e 38 objetos ilustrados).

---

## 2. Organização em Camadas dentro do `index.html`

O arquivo `index.html` está estruturado em três blocos progressivos claramente delimitados por comentários HTML:

1. **Estrutura Base (HTML + Design System CSS + Motor Inicial):**
   - Cabeçalho institucional (`<header>`), tela inicial (`<main id="home">`), tela de missão (`<main id="game">`), rodapé técnico (`<footer>`) e sistema de diálogo modal (`<div id="overlay">`).
   - Variáveis de identidade visual em `:root`:
     - `--ink: #20294a` (azul-marinho institucional para tipografia principal)
     - `--muted: #69728b` (texto secundário)
     - `--purple: #7655cb` (destaque principal / botões primários)
     - `--cyan: #12b8dc` (barra de progresso, foco de teclado e borda de feedback)
     - `--green: #a4cf43` (indicadores positivos)

2. **`<!-- CAMPAIGN V2 -->` (Motor de Campanha, Revisão Espaçada e Acessibilidade):**
   - Registro declarativo dos 38 riscos ocupacionais via `risk(id, name, tip, hint, kind)` no dicionário `R`.
   - Matriz `configs` com os 9 cenários ocupacionais (título, ícone, subtítulo, conquista, lista de 7 riscos e cor de parede).
   - Definição dos 3 níveis (`tiers`) e seleção automática de índices para revisão espaçada.
   - Construtor vetorial `object(kind, bad)` que desenha cada um dos 38 itens em suas duas versões: estado de risco (`bad = true`) e estado corrigido (`bad = false`).
   - Compositor de cena `campaignSvg(i, lv, decor)` em `viewBox="0 0 720 550"` posicionando os 7 slots em grade espacial:
     - Linha superior: `[14, 120]`, `[254, 120]`, `[494, 120]`
     - Linha intermediária: `[14, 263]`, `[254, 263]`, `[494, 263]`
     - Linha inferior central: `[254, 407]`

3. **`<!-- VISUAL V3 -->` (Renderização Ilustrada com Volume e Zoom):**
   - Sobrescreve de forma modular `object()` e `campaignSvg()` preservando toda a lógica da campanha:
     - Converte cores sólidas (`fill="#rrggbb"`) em gradientes lineares dinâmicos (`<linearGradient>`) calculados por `tone(hex, delta)` para simular luz e volume.
     - Aplica sombra projetada suave (`<feDropShadow>`) e elipse de contato no piso.
     - Injeta `details(kind, bad)` com rótulos, brilhos, manômetros, texturas e sinalizações de segurança em cada objeto.
     - Adiciona perspectiva de piso quadriculado, rodapé e iluminação lateral de janela.
   - Injeta a barra `.view-tools` com o botão **`⊕ Ampliar objetos`** (`toggleZoom()`), que expande o SVG para `160%` (desktop) ou `180%` (telas até `650px`) com rolagem horizontal suave (`overflow-x: auto`).

---

## 3. Persistência de Progresso (`localStorage`)

O estado do jogador é persistido localmente sob a chave `performance-campanha-v2`:

```json
{
  "done": ["0-0", "0-1", "1-2"],
  "states": {
    "1-2": [0],
    "6-2": [0, 2]
  }
}
```

- `done`: lista de chaves `"<indiceCenario>-<indiceNivel>"` já concluídas (de `0-0` até `8-2`, totalizando 27 missões).
- `states`: mapa de descobertas parciais por cenário/nível, permitindo retomar uma missão interrompida exatamente do ponto em que parou.
- Todas as leituras/gravações em `localStorage` são protegidas por blocos `try/catch`, garantindo funcionamento normal mesmo em navegação anônima restrita ou `WebViews` bloqueadas.

---

## 4. Recursos de Acessibilidade (A11y)

- **Teclado completo:** todos os objetos ativos da cena possuem `role="button"`, `tabindex="0"` e acionamento via `Enter` ou `Espaço`.
- **Foco visível:** contorno de alto contraste (`outline: 3px solid #12b8dc`) em `:focus-visible`.
- **Modais acessíveis:** `role="dialog"`, `aria-modal="true"`, `aria-labelledby="modalTitle"`, fechamento por `Escape`, ciclo de foco (*focus trap* com `Tab` / `Shift+Tab`) e restauração automática do foco ao elemento anterior ao fechar.
- **Leitores de tela:** painel de feedback com `aria-live="polite"` e atualização dinâmica de `aria-label` / `aria-disabled="true"` quando um risco é solucionado (`"Resolvido: <nome do risco>"`).

---

## 5. Como Editar Textos ou Cenários

Para ajustar um texto durante a revisão técnica de SST:

1. Abra o arquivo `index.html` em qualquer editor de código (como VS Code).
2. Localize a chamada `risk('<codigo>', ...)` dentro da seção `<!-- CAMPAIGN V2 -->`.
3. Edite os parâmetros desejados:
   ```js
   risk(
     'sharps',
     'Perfurocortante fora do coletor', // Título curto exibido no feedback e no chip
     'Descarte perfurocortantes imediatamente após o uso em coletor apropriado, seguindo os procedimentos do serviço.', // Orientação preventiva
     'Há uma agulha deixada na bandeja.' // Pista exibida ao pedir ajuda
   );
   ```
4. Salve o arquivo, atualize o navegador para validar e sincronize a alteração na tabela de referência em [`docs/GUIA_PEDAGOGICO_SST.md`](GUIA_PEDAGOGICO_SST.md).
