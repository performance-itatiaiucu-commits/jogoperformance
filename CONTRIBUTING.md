# Guia de Contribuição e Manutenção

Este documento orienta colaboradores, revisores técnicos de Saúde e Segurança do Trabalho (SST) e desenvolvedores autorizados pelo **Grupo Performance Ocupacional** na manutenção e evolução do projeto **Olho Vivo**.

---

## Fluxo de Trabalho Recomendado

1. **Crie uma branch dedicada** a partir da `main` para cada melhoria ou revisão técnica:
   - Conteúdo/SST: `conteudo/revisao-clinica-cenario-7`
   - Visual/UI: `melhoria/contraste-botoes-mobile`
   - Correção: `correcao/ajuste-pista-escada`
2. **Realize e valide as alterações localmente** abrindo o `index.html` em tamanhos de tela desktop e celular.
3. **Abra um Pull Request (PR)** descrevendo claramente:
   - O que foi alterado;
   - Qual cenário ou risco ocupacional foi impactado;
   - Capturas de tela antes/depois (quando houver mudança visual).
4. **Revisão técnica:** alterações em orientações de prevenção devem passar pela validação técnica de SST da clínica antes da publicação na `main`.

---

## Diretrizes de Conteúdo e Linguagem (SST)

Ao editar ou criar novos riscos e orientações em [`docs/GUIA_PEDAGOGICO_SST.md`](docs/GUIA_PEDAGOGICO_SST.md) e no `index.html`:

- **Tom acolhedor e educativo:** evite linguagem punitiva ou alarmista; valorize a observação atenta e o cuidado mútuo (*"Prevenir é cuidar"*).
- **Clareza e objetividade:** mantenha os títulos curtos e as dicas de prevenção diretas (1 a 2 frases claras para leitura rápida no celular).
- **Rigor técnico responsável:** oriente sempre boas práticas gerais alinhadas às normas de segurança, lembrando que intervenções específicas dependem dos procedimentos do local e de profissionais habilitados/autorizados.

---

## Checklist de Qualidade antes do Merge

- [ ] Todos os **9 cenários** abrem corretamente nos **3 níveis** (Primeiro olhar, Olhar atento e Olhar de especialista).
- [ ] Ao tocar em cada risco ativo, o objeto alterna do estado de risco (`.danger`) para o estado seguro (`.safe`) com o selo de confirmação.
- [ ] O botão **`⊕ Ampliar objetos`** funciona corretamente em telas móveis com rolagem horizontal suave.
- [ ] O botão **`✦ Quero uma pista`** respeita o comportamento pedagógico de cada nível.
- [ ] O botão **`Ⅱ Fui chamado!`** pausa e retoma a partida mantendo o foco acessível.
- [ ] A navegação por teclado (`Tab`, `Enter`, `Espaço` e `Esc`) permanece funcional.
- [ ] Nenhum arquivo temporário de log (`*.log`) foi incluído no commit.
