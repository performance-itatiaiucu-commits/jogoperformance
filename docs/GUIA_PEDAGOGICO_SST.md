# Guia Pedagógico e Catálogo de Riscos (SST)

> **Projeto:** Olho Vivo — *Diversão que vira prevenção*  
> **Instituição:** Grupo Performance Ocupacional · Saúde e Segurança do Trabalho  
> **Finalidade deste documento:** apoiar a equipe técnica de SST, instrutores e revisores clínicos na validação pedagógica, uso em campanhas (SIPAT, integrações, salas de espera, ações educativas) e evolução dos conteúdos.

---

## 1. Proposta Pedagógica

O **Olho Vivo** transforma a percepção de riscos ocupacionais em uma atividade rápida, leve e acessível diretamente no celular ou computador:

- **Aprendizagem sem pressão:** não há cronômetro regressivo nem perda de pontos ao tocar em objetos seguros — o erro é tratado como parte natural da observação exploratória.
- **Transformação positiva do ambiente:** a cada risco identificado, a ilustração não apenas marca um acerto, mas **corrige visualmente a situação** (por exemplo: a gaveta é fechada, o cilindro recebe corrente de fixação, a abertura no piso ganha guarda-corpo, o perfurocortante vai para o coletor adequado).
- **Respeito à rotina real:** o botão **`Ⅱ Fui chamado!`** permite pausar imediatamente a atividade (ideal para colaboradores em intervalo ou pacientes aguardando atendimento na clínica), mantendo o progresso salvo localmente.

---

## 2. Estrutura de Níveis e Revisão Espaçada

Cada um dos **9 ambientes** possui **7 objetos posicionados** na cena e se divide em **3 níveis progressivos** (totalizando **27 missões**):

| Nível | Nome | Qtd. de Riscos | Posições Ativas (`indices`) | Estratégia de Pistas (`✦ Quero uma pista`) |
| :---: | :--- | :---: | :---: | :--- |
| **1** | 🌱 **Primeiro olhar** | 3 riscos | `[0, 1, 2]` | **Pista direta + destaque visual:** exibe dica objetiva e aplica animação pulsante no objeto correspondente. |
| **2** | 🔎 **Olhar atento** | 4 riscos | `[3, 4, 5, 6]` | **Novos detalhes + pista textual:** apresenta 4 riscos inéditos do ambiente e fornece orientação textual sem entregar visualmente o brilho. |
| **3** | ⚡ **Olhar de especialista** | 5 riscos | `[0, 2, 3, 5, 6]` | **Revisão espaçada + combinação:** reúne situações vistas nos Níveis 1 e 2. Ao pedir ajuda, incentiva primeiro o raciocínio preventivo e oferece o botão opcional *"Revelar uma pista →"*. |

---

## 3. Matriz dos 9 Cenários e Conquistas

| # | Ambiente | Frase-Tema | Conquista (Nível 3) | Nível 1 (`0,1,2`) | Nível 2 (`3,4,5,6`) | Nível 3 (`0,2,3,5,6`) |
| :-: | :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | 🖥️ **Escritório em alerta** | *O perigo também usa roupa de escritório.* | 🏆 Olhar de águia | `cable`, `exit`, `spill` | `drawer`, `stack`, `socket`, `chair` | `cable`, `spill`, `drawer`, `socket`, `chair` |
| **2** | 🛠️ **Oficina organizada** | *Ferramentas no lugar. Atenção nos detalhes.* | 🏆 Mestre da oficina | `tools`, `exit`, `spill` | `stack`, `extinguisher`, `guard`, `bottle` | `tools`, `spill`, `stack`, `guard`, `bottle` |
| **3** | 🍳 **Cozinha sem sustos** | *A receita certa começa na prevenção.* | 🏆 Chef da prevenção | `pan`, `spill`, `knife` | `cloth`, `box`, `socket`, `bottle` | `pan`, `knife`, `cloth`, `socket`, `bottle` |
| **4** | 🏗️ **Construção consciente** | *Cada etapa merece um olhar atento.* | 🏆 Guardião da obra | `ladder`, `edge`, `nails` | `cable`, `stack`, `suspended`, `exit` | `ladder`, `nails`, `cable`, `suspended`, `exit` |
| **5** | 📦 **Estoque em ordem** | *Organização que abre caminhos.* | 🏆 Expert da organização | `stack`, `box`, `extinguisher` | `shelf`, `route`, `heavy`, `exit` | `stack`, `extinguisher`, `shelf`, `heavy`, `exit` |
| **6** | 🧹 **Limpeza com cuidado** | *Tudo limpo. Nada de improviso.* | 🏆 Agente do cuidado | `spill`, `bottle`, `mix` | `cart`, `damaged`, `box`, `socket` | `spill`, `mix`, `cart`, `box`, `socket` |
| **7** | 🩺 **Clínica mais segura** | *Cuidar de quem cuida também importa.* | 🏆 Aliado do cuidado | `sharps`, `fullbin`, `food` | `spill`, `cylinder`, `exit`, `cable` | `sharps`, `food`, `spill`, `exit`, `cable` |
| **8** | 🚚 **Transporte atento** | *Prevenção acompanha cada trajeto.* | 🏆 Piloto da prevenção | `belt`, `phone`, `cargo` | `tire`, `box`, `step`, `extinguisher` | `belt`, `cargo`, `tire`, `step`, `extinguisher` |
| **9** | 🌤️ **Trabalho ao ar livre** | *Um olhar atento, faça chuva ou sol.* | 🏆 Explorador consciente | `heat`, `storm`, `water` | `edge`, `sign`, `tools`, `ladder` | `heat`, `water`, `edge`, `tools`, `ladder` |

---

## 4. Catálogo Completo dos 38 Riscos Ocupacionais (Referência para Revisão Técnica)

A tabela abaixo lista integralmente os textos atualmente configurados na aplicação para facilitar revisões pela equipe técnica de SST da clínica:

| Código | Situação de Risco | Orientação Preventiva Exibida ao Jogador | Pista Pedagógica |
| :--- | :--- | :--- | :--- |
| `cable` | **Cabo na circulação** | Organize os cabos fora das passagens. Um caminho livre reduz o risco de tropeços. | Procure uma linha escura atravessando o chão. |
| `exit` | **Saída bloqueada** | Mantenha as rotas de saída desobstruídas. Materiais precisam de um local próprio. | Observe a área em frente à porta verde. |
| `spill` | **Líquido no piso** | Sinalize ou isole a área e providencie a limpeza conforme o produto e os procedimentos do local. | Procure um reflexo azulado no chão. |
| `drawer` | **Gaveta aberta** | Feche as gavetas após o uso para evitar choques e tropeços na circulação. | Um móvel está com uma parte projetada para fora. |
| `stack` | **Pilha instável** | Empilhe materiais sobre base estável, respeitando os limites de altura e carga. | Há caixas inclinadas, fora de alinhamento. |
| `socket` | **Tomada sobrecarregada** | Evite improvisos e o acúmulo de adaptadores. A instalação deve ser avaliada por profissional habilitado. | Veja quantos adaptadores foram ligados no mesmo ponto. |
| `chair` | **Subida improvisada** | Não use cadeira como escada. Utilize equipamento de acesso adequado à tarefa e às condições do local. | Uma cadeira com rodinhas está sendo usada para alcançar o alto. |
| `tools` | **Ferramentas no chão** | Guarde ferramentas em suportes ou locais próprios, sem bloquear a circulação. | Há ferramentas longe da bancada. |
| `extinguisher` | **Extintor bloqueado** | Mantenha o extintor visível e com acesso desobstruído, conforme o projeto de segurança do local. | Veja o que está na frente do equipamento vermelho. |
| `guard` | **Proteção de máquina ausente** | Não opere máquinas sem as proteções exigidas. Intervenções devem seguir procedimentos de segurança e ser feitas por pessoas autorizadas. | A lâmina da máquina está exposta. |
| `bottle` | **Produto sem identificação** | Mantenha produtos químicos identificados e em embalagens apropriadas. Não use garrafas de bebidas para armazená-los. | Uma garrafa de bebida parece estar guardando um produto de limpeza. |
| `pan` | **Cabo da panela na passagem** | Posicione cabos de panelas para não se projetarem na passagem, evitando também outras fontes de calor. | O cabo da panela aponta para fora do fogão. |
| `knife` | **Faca na borda** | Mantenha facas longe das bordas e guarde-as em suporte adequado após o uso. | Observe onde a faca foi deixada. |
| `cloth` | **Pano junto à chama** | Afaste panos e outros materiais combustíveis de chamas e superfícies quentes. | Um tecido está muito perto do fogo. |
| `box` | **Passagem obstruída** | Armazene caixas fora das áreas de circulação, mantendo o caminho desimpedido. | Uma caixa está bem no meio do caminho. |
| `ladder` | **Escada danificada** | Não utilize escadas danificadas. Retire-as de uso e comunique o responsável para avaliação e substituição. | Observe os degraus da escada. |
| `edge` | **Abertura sem proteção** | Aberturas e bordas devem ter proteção coletiva adequada. Isole a área e comunique o responsável. | Há uma abertura no piso sem proteção. |
| `nails` | **Pregos expostos** | Recolha e destine materiais com pontas expostas de modo seguro, conforme os procedimentos do local. | Observe a madeira no chão. |
| `suspended` | **Carga suspensa sobre passagem** | Não permaneça nem circule sob cargas suspensas. Respeite o isolamento da área de movimentação. | Veja o caminho abaixo da carga suspensa. |
| `shelf` | **Prateleira danificada** | Retire estruturas danificadas de uso e solicite avaliação. Respeite a capacidade e a distribuição de carga. | Uma prateleira está cedendo sob os materiais. |
| `route` | **Pedestre na rota de empilhadeira** | Use as rotas de pedestres e respeite a segregação e os procedimentos de movimentação do local. | Observe onde o pedestre está em relação à empilhadeira. |
| `heavy` | **Volume pesado no alto** | Planeje o armazenamento considerando peso, frequência de uso e meios auxiliares. Evite volumes pesados em posições que dificultem o manuseio. | A caixa de 30 kg está no ponto mais alto. |
| `mix` | **Mistura de produtos** | Não misture produtos de limpeza. Siga o rótulo e as orientações de segurança: misturas podem liberar gases perigosos. | Duas embalagens diferentes estão sendo despejadas no mesmo balde. |
| `cart` | **Carrinho bloqueando rota** | Estacione carrinhos em locais próprios, sem bloquear portas ou áreas de circulação. | Observe onde o carrinho foi estacionado. |
| `damaged` | **Cabo elétrico danificado** | Retire o equipamento de uso e comunique o responsável. Reparos devem ser feitos por pessoa autorizada; não improvise emendas. | Um fio está com os condutores aparentes. |
| `sharps` | **Perfurocortante fora do coletor** | Descarte perfurocortantes imediatamente após o uso em coletor apropriado, seguindo os procedimentos do serviço. | Há uma agulha deixada na bandeja. |
| `fullbin` | **Coletor acima do limite** | Substitua o coletor ao atingir o limite indicado pelo fabricante. Nunca force materiais para dentro. | Observe o limite de enchimento do coletor. |
| `food` | **Alimento na área de procedimentos** | Mantenha alimentos e bebidas fora das áreas de procedimentos e de exposição a agentes biológicos. | Um lanche apareceu perto dos materiais de atendimento. |
| `cylinder` | **Cilindro sem fixação** | Mantenha cilindros na posição e com a fixação apropriadas, conforme as orientações do fornecedor e os procedimentos do local. | Um cilindro alto está sem suporte ou corrente. |
| `belt` | **Cinto não afivelado** | Antes de iniciar o deslocamento, afivele o cinto de segurança e verifique que todos os ocupantes também o utilizem. | Observe a faixa de proteção no banco do motorista. |
| `phone` | **Celular ao dirigir** | Não manuseie o celular ao dirigir. Para utilizá-lo, pare em local permitido e seguro. | Há um celular na mão do motorista. |
| `cargo` | **Carga sem amarração** | Acondicione e fixe a carga com meios adequados, respeitando os limites do veículo e as regras aplicáveis. | Veja se as caixas estão presas no compartimento de carga. |
| `tire` | **Pneu visivelmente danificado** | Antes de usar o veículo, faça as verificações previstas. Ao identificar dano no pneu, não siga viagem sem avaliação e correção. | Observe a lateral do pneu. |
| `step` | **Degrau danificado** | Não use acessos danificados. Isole ou sinalize o local e providencie a correção antes de liberar a passagem. | Um degrau está quebrado na entrada. |
| `storm` | **Atividade exposta a raios** | Ao perceber risco de tempestade com raios, interrompa a atividade exposta e procure abrigo seguro, seguindo o plano local. Árvore isolada não é abrigo seguro. | Há uma pessoa ao ar livre durante uma tempestade. |
| `water` | **Recipiente de água aberto** | Mantenha recipientes de água tampados e elimine água parada, seguindo as orientações de prevenção a vetores. | Observe o recipiente descoberto. |
| `heat` | **Sem planejamento para o calor** | Em trabalho sob calor, planeje hidratação, pausas e outras medidas conforme avaliação do risco e orientação da equipe de SST. | O posto ao sol está sem água disponível nem área de pausa. |
| `sign` | **Área de trabalho sem isolamento** | Delimite e sinalize a área conforme a atividade, protegendo trabalhadores e pessoas que circulam no entorno. | Um serviço na calçada está misturado com a passagem de pedestres. |

---

## 5. Sugestões de Aplicação Prática

1. **Sala de Espera da Clínica (QR Code):** cartaz ou display com QR Code levando ao link do jogo enquanto colaboradores aguardam exames ocupacionais (admissionais, periódicos, retorno ao trabalho).
2. **SIPAT e Campanhas Temáticas:** desafio por equipes escolhendo o cenário mais próximo da atividade da empresa cliente (ex.: *Construção consciente*, *Estoque em ordem*, *Clínica mais segura*, *Transporte atento*).
3. **Integração de Novos Colaboradores:** aquecimento dinâmico de 5 minutos antes de treinamentos introdutórios de segurança para despertar a percepção de riscos cotidianos.
