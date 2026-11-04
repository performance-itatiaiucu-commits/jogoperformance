# Histórico de Versões (Changelog)

Todas as mudanças relevantes do projeto **Olho Vivo • Grupo Performance Ocupacional** são documentadas neste arquivo.

O formato segue os princípios do [Keep a Changelog](https://keepachangelog.com/pt-BR/1.0.0/).

---

## [3.0.0] - 2026-11-04

### Adicionado
- **Camada Visual Ilustrada (`VISUAL V3`):** aplicação de volume, iluminação consistente, sombras suaves (`feDropShadow`), gradientes dinâmicos de materiais e detalhes funcionais em todos os 38 objetos SVG.
- **Ambientação com perspectiva:** piso quadriculado com linhas de profundidade, rodapé, iluminação de janela e identificação visual dos ambientes.
- **Ferramenta de Zoom (`⊕ Ampliar objetos`):** alternância entre visão completa e visualização ampliada (`160%` no desktop e `180%` no mobile) com rolagem horizontal suave, preservando dicas e descobertas sincronizadas.
- **Documentação oficial do repositório:** `README.md`, `LICENSE` institucional, `.gitignore`, `CONTRIBUTING.md`, `SECURITY.md`, guia pedagógico completo (`docs/GUIA_PEDAGOGICO_SST.md`) e documentação de arquitetura (`docs/ARQUITETURA_TECNICA.md`).

---

## [2.0.0] - Campanha Ampliada (`CAMPAIGN V2`)

### Adicionado
- **Expansão para 9 cenários ocupacionais:**
  1. Escritório em alerta
  2. Oficina organizada
  3. Cozinha sem sustos
  4. Construção consciente
  5. Estoque em ordem
  6. Limpeza com cuidado
  7. Clínica mais segura
  8. Transporte atento
  9. Trabalho ao ar livre
- **Progressão em 3 níveis por ambiente (27 missões no total)** com metodologia de **revisão espaçada**:
  - *Nível 1 — Primeiro olhar* (3 riscos e destaque visual na pista);
  - *Nível 2 — Olhar atento* (4 novos detalhes e pista textual);
  - *Nível 3 — Olhar de especialista* (5 riscos combinando aprendizados anteriores com reflexão guiada).
- **Catálogo de 38 riscos ocupacionais** com ilustrações vetoriais duplas (estado de risco e estado corrigido).
- **Melhorias de acessibilidade:** gerenciamento de foco ao abrir/fechar modais (`Tab` trap e tecla `Escape`), atributos `aria-label`, `aria-disabled` e região `aria-live="polite"` para leitores de tela.
- **Persistência de campanha (`performance-campanha-v2`)** no `localStorage` com indicadores visuais de progresso por cartão.

---

## [1.0.0] - Protótipo Base

### Adicionado
- Estrutura inicial do jogo educativo **Olho Vivo — Cadê o perigo?** com identidade visual do **Grupo Performance Ocupacional**.
- Três ambientes iniciais (Escritório, Oficina e Cozinha), sistema de feedback educativo imediato, conquistas e recurso de pausa rápida (`Ⅱ Fui chamado!`).
