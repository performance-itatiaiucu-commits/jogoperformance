# Política de Segurança e Privacidade (LGPD)

## Privacidade por Padrão

O projeto **Olho Vivo • Grupo Performance Ocupacional** foi projetado com arquitetura **100% estática no navegador (*client-side*)**, priorizando simplicidade, segurança e conformidade com a **Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)**:

- **Sem cadastro ou login:** nenhum dado pessoal (nome, CPF, e-mail, telefone ou empresa) é solicitado para jogar.
- **Sem servidor de banco de dados:** nenhuma informação de uso é transmitida para servidores externos.
- **Sem cookies de rastreamento ou bibliotecas de terceiros:** o aplicativo não carrega scripts externos, CDNs ou ferramentas invasivas de *analytics*.
- **Armazenamento estritamente local:** o progresso das missões concluídas fica salvo apenas no `localStorage` do próprio navegador do dispositivo (`performance-campanha-v2`), podendo ser apagado a qualquer momento limpando os dados do navegador.

---

## Superfície Técnica de Segurança

- Aplicação composta por arquivo único autônomo (`index.html`), utilizando apenas HTML5, CSS3, JavaScript nativo e gráficos vetoriais SVG embutidos.
- Compatível com hospedagem estática sob **HTTPS** (como GitHub Pages, servidores corporativos internos, totens interativos ou acesso offline local).
- Caso o aplicativo seja integrado futuramente a portais internos ou sistemas com autenticação, recomenda-se configurar cabeçalhos HTTP padrão de proteção (`Content-Security-Policy`, `X-Content-Type-Options: nosniff` e `Referrer-Policy: strict-origin-when-cross-origin`).

---

## Como Reportar Problemas de Segurança

Caso identifique qualquer vulnerabilidade técnica, falha de exibição ou uso indevido de marca/conteúdo:

1. Evite divulgar detalhes sensíveis publicamente antes da análise técnica.
2. Entre em contato diretamente com a equipe responsável do **Grupo Performance Ocupacional** ou registre uma comunicação interna para avaliação e correção imediata.
