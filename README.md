# Projeto Integrador - Modelo
*(Coloque aqui o nome do seu projeto.)*

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.
*(Coloque aqui uma breve descrição do seu projeto.)*

**IMPORTANTE**: [**Cadastre seu projeto nesta planilha**](https://docs.google.com/spreadsheets/d/1bSb1-S9qOf46fNH8quyoFpcjcTuBMj_EdSPchOuFULY/edit?usp=sharing).

Professor: [Marco André Mendes](github.com/marcoandre)

Equipe:
- [Rodolpho da Silva Rocha](github.com/rodolphorocha)
- [Vitor Manoel Silva Santana](github.com/vitormsantanaa)
- [Vitória de Souza](github.com/vitoriadesouza)

Links do projeto:
(*Coloque aqui os links para a documentação do projeto e os repositórios e plubicação do backend e frontend.*)
-   Documentação [(esse documento)](github.com/vitoriadesouza/OPES)
-   Backend: [Repositório](github.com/vitormsantanaa/backend-opes) e [Publicação](https://pi-backend.herokuapp.com/)
-   Frontend: [Repositório](github.com/vitormsantanaa/frontend-opes) e [Publicação](https://pi-frontend.herokuapp.com/)


# 1. Descrição do Projeto
O objetivo do site seria oferecer serviços de consultoria financeira personalizada. Os usuários poderiam receber orientações sobre como planejar suas finanças pessoais, economizar, investir, planejar para a aposentadoria ou até mesmo gerenciar dívidas e impostos.
Principais tipos de consultoria que o site vai oferecer:

**1.1.1 - Consultoria Pessoal**: Auxiliar indivíduos a controlarem seus orçamentos, economizarem para objetivos de curto, médio e longo prazo (como comprar uma casa, pagar dívidas, viajar, ou guardar para a aposentadoria).

**1.1.2 - Consultoria para Investimentos:** Orientar sobre como investir de maneira inteligente, considerando o perfil de risco de cada cliente, seja em ações, imóveis, fundos, ou outras alternativas de investimento.

**1.1.3 - Planejamento para Aposentadoria:** Auxiliar clientes a se prepararem para a aposentadoria com planejamento adequado de poupança e investimentos.

**1.1.4 - Gestão de Dívidas:** Ajudar a criar estratégias para quitar dívidas de forma eficiente e melhorar o crédito.

# 2. Situação Problema

O trabalho OPES apresenta uma solução tecnológica voltada ao controle financeiro pessoal e familiar, com o objetivo de facilitar a organização e o acompanhamento das finanças de usuários de diferentes perfis. Desenvolvido por Rodolpho da Silva Rocha, Vitor Manoel Silva Santana e Vitória de Souza, o sistema busca centralizar informações sobre receitas, despesas, cartões, carteiras, investimentos e metas financeiras em uma única plataforma. Apesar de ser um projeto recente, o OPES se propõe a oferecer recursos intuitivos e seguros, permitindo que indivíduos e famílias planejem seu orçamento de forma eficiente, acompanhem seu progresso financeiro e tomem decisões mais conscientes sobre seus recursos.

Muitas pessoas enfrentam dificuldades para manter o controle de suas finanças pessoais no dia a dia. A falta de organização, o desconhecimento sobre para onde o dinheiro está indo e a ausência de planejamento financeiro acabam resultando em gastos desnecessários, endividamento e insegurança econômica.
Grande parte das soluções disponíveis no mercado é complexa, pouco intuitiva ou não atende às necessidades reais dos usuários, especialmente aqueles que não possuem conhecimento financeiro avançado. Isso faz com que muitas pessoas desistam de utilizar ferramentas de controle ou continuem utilizando métodos ineficientes, como anotações manuais ou planilhas desatualizadas.

Analisando a situação atual, fica evidente que a dispersão de informações financeiras e a falta de centralização dificultam o controle e planejamento financeiro. O uso de um software de gestão financeira, como o proposto pelo OPES, poderia resolver esses problemas ao consolidar dados de receitas, despesas, cartões, carteiras e investimentos em uma única plataforma. Com recursos como dashboards, relatórios e acompanhamento de metas, o sistema permite uma visão clara e atualizada das finanças, tornando o gerenciamento mais eficiente, seguro e confiável, além de facilitar a tomada de decisões estratégicas para o futuro financeiro dos usuários.


# 3. Descrição da proposta

O OPES é um sistema de controle financeiro pessoal e familiar, focado em organizar receitas, despesas, cartões, carteiras, investimentos e metas financeiras em um só lugar. Com o OPES, será possível cadastrar receitas e despesas, acompanhar faturas de cartões, gerenciar múltiplas carteiras e monitorar investimentos e metas financeiras, além de visualizar dashboards e relatórios gráficos que facilitam o acompanhamento da situação financeira e a tomada de decisões.

# 4. Modelagem de Dados

![Modelagem de Dados](img/bd.png)



# 4. Regras de negócio

- **RN01 – Permissão de Administrador:** Apenas administradores podem adicionar/remover membros.
- **RN02 – Pertencimento a Grupo:** Cada usuário deve pertencer a pelo menos um grupo familiar.
- **RN03 – Restrição de Exclusão:** Membros com permissão limitada não podem excluir dados.
- **RN04 – Despesa Afeta Saldo:** Toda despesa deve reduzir o saldo da carteira associada.
- **RN05 – Receita Afeta Saldo:** Toda receita deve aumentar o saldo da carteira.
- **RN06 – Validação de Valor:** Transações não podem ter valor negativo.
- **RN07 – Categoria Obrigatória:** Uma transação deve sempre estar vinculada a uma categoria.
- **RN08 – Limite do Cartão:** O valor total da fatura não pode ultrapassar o limite do cartão.
- **RN09 – Despesa Futura no Cartão:** Compras no cartão devem ser registradas como despesa futura.
- **RN10 – Saldo Total Consistente:** Transferências entre carteiras devem manter o saldo total consistente.
- **RN11 – Saldo Negativo Permitido:** Não é permitido saldo negativo, salvo se configurado (ex: conta corrente).
- **RN12 – Cálculo de Rendimento:** O rendimento deve ser calculado com base no valor investido.
- **RN13 – Investimento Positivo:** Investimentos não podem ter valores negativos.
- **RN14 – Atualização de Saldo:** Resgates devem atualizar automaticamente o saldo da carteira.
- **RN15 – Validação de Meta:** O valor atual da meta não pode ultrapassar o valor alvo.
- **RN16 – Atualização Automática da Meta:** O progresso da meta deve ser atualizado automaticamente.


# 5. Requisitos funcionais

Este documento descreve os requisitos funcionais do sistema financeiro, organizados em **Entradas**, **Processos** e **Saídas**.

---

## Entradas

### R.F.01 – Cadastro de Usuários
- **Descrição:** Permitir cadastrar usuários no sistema para que possam acessar suas funcionalidades.
- **Dados necessários:** nome, email, senha, nível de permissão
- **Usuários:** Administrador

### R.F.02 – Login e Logout
- **Descrição:** Permitir que usuários façam login e logout, garantindo acesso seguro.
- **Dados necessários:** login, senha
- **Usuários:** Todos os níveis de usuário

### R.F.03 – Criação de Grupos Familiares
- **Descrição:** Permitir criar grupos familiares para organizar usuários por família.
- **Dados necessários:** nome do grupo, membros associados
- **Usuários:** Administrador

### R.F.04 – Adição/Remoção de Membros da Família
- **Descrição:** Permitir adicionar ou remover membros de um grupo familiar.
- **Dados necessários:** nome do usuário, grupo familiar
- **Usuários:** Administrador

### R.F.05 – Definição de Permissões por Membro
- **Descrição:** Permitir definir permissões individuais para membros de um grupo familiar.
- **Dados necessários:** usuário, nível de permissão
- **Usuários:** Administrador

### R.F.06 – Cadastro de Receitas
- **Descrição:** Permitir registrar receitas financeiras do usuário.
- **Dados necessários:** valor, categoria, data, carteira associada
- **Usuários:** Todos os níveis de usuário

### R.F.07 – Cadastro de Despesas
- **Descrição:** Permitir registrar despesas financeiras do usuário.
- **Dados necessários:** valor, categoria, data, carteira associada
- **Usuários:** Todos os níveis de usuário

### R.F.10 – Categorizar Transações
- **Descrição:** Permitir classificar transações em categorias, como alimentação, transporte, etc.
- **Dados necessários:** transação, categoria
- **Usuários:** Todos os níveis de usuário

### R.F.11 – Anexar Descrição e Data às Transações
- **Descrição:** Permitir adicionar informações detalhadas às transações.
- **Dados necessários:** descrição, data, transação
- **Usuários:** Todos os níveis de usuário

### R.F.12 – Recorrência de Transações
- **Descrição:** Permitir definir recorrência de transações (mensal, semanal).
- **Dados necessários:** transação, frequência
- **Usuários:** Todos os níveis de usuário

### R.F.13 – Cadastro de Cartões de Crédito/Débito
- **Descrição:** Permitir registrar cartões para controle de despesas futuras e limites.
- **Dados necessários:** número do cartão, tipo, limite, titular
- **Usuários:** Todos os níveis de usuário

### R.F.14 – Definir Limite de Crédito
- **Descrição:** Permitir definir o limite máximo de cada cartão.
- **Dados necessários:** cartão, limite
- **Usuários:** Todos os níveis de usuário

### R.F.18 – Criação de Carteiras
- **Descrição:** Permitir criar múltiplas carteiras (dinheiro, conta bancária, etc.) para organizar finanças.
- **Dados necessários:** nome da carteira, saldo inicial
- **Usuários:** Todos os níveis de usuário

### R.F.21 – Cadastro de Investimentos
- **Descrição:** Permitir registrar investimentos realizados pelo usuário.
- **Dados necessários:** tipo de investimento, valor, data, carteira associada
- **Usuários:** Todos os níveis de usuário

### R.F.25 – Criação de Metas Financeiras
- **Descrição:** Permitir criar metas financeiras para planejamento de objetivos.
- **Dados necessários:** nome da meta, valor alvo, prazo, carteira ou investimento vinculado
- **Usuários:** Todos os níveis de usuário

---

## Processos

### R.F.08 – Manutenção de Transações
- **Descrição:** Registrar, manter e validar todas as transações do usuário.
- **Dados necessários:** valor, tipo (receita/despesa), categoria, data, carteira
- **Usuários:** Todos os níveis de usuário

### R.F.09 – Edição e Exclusão de Transações
- **Descrição:** Permitir alterar ou remover transações registradas.
- **Dados necessários:** transação selecionada, alterações
- **Usuários:** Todos os níveis de usuário (com permissão)

### R.F.15 – Registro de Gastos por Cartão
- **Descrição:** Registrar automaticamente despesas feitas por cartão para controle financeiro.
- **Dados necessários:** cartão, valor, data, categoria
- **Usuários:** Todos os níveis de usuário

### R.F.16 – Cálculo Automático de Faturas
- **Descrição:** Calcular automaticamente o valor total das faturas com base nas compras registradas.
- **Dados necessários:** histórico de compras, cartão
- **Usuários:** Todos os níveis de usuário

### R.F.19 – Transferências Entre Carteiras
- **Descrição:** Permitir transferir valores entre diferentes carteiras do usuário, mantendo saldo consistente.
- **Dados necessários:** carteira origem, carteira destino, valor
- **Usuários:** Todos os níveis de usuário

### R.F.22 – Acompanhamento de Rendimento
- **Descrição:** Calcular e mostrar rendimento de investimentos registrados.
- **Dados necessários:** investimento, valor inicial, rendimento calculado
- **Usuários:** Todos os níveis de usuário

### R.F.26 – Definir Valor Alvo e Prazo da Meta
- **Descrição:** Calcular e atualizar metas com base em valor alvo e prazo definidos.
- **Dados necessários:** meta, valor alvo, prazo
- **Usuários:** Todos os níveis de usuário

### R.F.28 – Vincular Metas a Carteiras ou Investimentos
- **Descrição:** Associar metas a carteiras ou investimentos, permitindo acompanhamento automático.
- **Dados necessários:** meta, carteira/investimento vinculado
- **Usuários:** Todos os níveis de usuário

---

## Saídas

### R.F.17 – Visualização de Faturas
- **Descrição:** Mostrar faturas abertas e fechadas com detalhamento de gastos.
- **Dados necessários:** fatura, cartão
- **Usuários:** Todos os níveis de usuário

### R.F.20 – Exibição de Saldo por Carteira
- **Descrição:** Exibir o saldo atualizado de cada carteira em tempo real.
- **Dados necessários:** carteira, saldo atualizado
- **Usuários:** Todos os níveis de usuário

### R.F.23 – Histórico de Valorização
- **Descrição:** Exibir histórico de valorização de investimentos ao longo do tempo.
- **Dados necessários:** investimento, datas, valores
- **Usuários:** Todos os níveis de usuário

### R.F.24 – Categorização de Tipos de Investimento
- **Descrição:** Mostrar investimentos classificados por categoria.
- **Dados necessários:** investimento, categoria
- **Usuários:** Todos os níveis de usuário

### R.F.27 – Exibição do Progresso da Meta
- **Descrição:** Mostrar progresso atual de metas financeiras.
- **Dados necessários:** meta, valor atual, valor alvo
- **Usuários:** Todos os níveis de usuário

### R.F.29 – Dashboard Resumido
- **Descrição:** Exibir resumo financeiro do usuário, incluindo saldos, investimentos e metas.
- **Dados necessários:** saldos, transações, metas, investimentos
- **Usuários:** Todos os níveis de usuário

# 6. Requisitos não funcionais

Este documento descreve os requisitos não funcionais do sistema financeiro, organizados por categoria.

---

## Desempenho

### R.N.F.01 – Tempo de Resposta
- **Descrição:** O sistema deve responder às ações do usuário em até 2 segundos em condições normais de uso.
- **Medição:** Testes de desempenho durante o uso com até 100 usuários simultâneos.
- **Usuários:** Todos os níveis de usuário

### R.N.F.02 – Processamento de Transações
- **Descrição:** As transações financeiras (receitas, despesas, transferências) devem ser processadas em tempo real ou quase real.
- **Medição:** Verificação de atualização de saldo em menos de 1 segundo.
- **Usuários:** Todos os níveis de usuário

---

## Segurança

### R.N.F.03 – Autenticação e Autorização
- **Descrição:** O sistema deve exigir login seguro com senha e nível de permissão para acessar funcionalidades.
- **Medição:** Tentativas de acesso não autorizado bloqueadas e registradas.
- **Usuários:** Todos os níveis de usuário

### R.N.F.04 – Criptografia de Dados
- **Descrição:** Dados sensíveis, como senha, número de cartão e saldo, devem ser armazenados criptografados.
- **Medição:** Verificação de armazenamento criptografado com algoritmo seguro (ex: AES-256).
- **Usuários:** Todos os níveis de usuário

### R.N.F.05 – Auditoria e Logs
- **Descrição:** Todas as ações críticas (criação/edição/exclusão de transações, transferências e login) devem ser registradas em logs para auditoria.
- **Medição:** Logs disponíveis e verificáveis pelo administrador.
- **Usuários:** Administrador

---

## Usabilidade

### R.N.F.06 – Interface Intuitiva
- **Descrição:** O sistema deve possuir interface amigável e intuitiva, permitindo navegação clara sem necessidade de treinamento avançado.
- **Medição:** Feedback positivo de pelo menos 90% dos usuários em testes de usabilidade.
- **Usuários:** Todos os níveis de usuário

---

## Compatibilidade

### R.N.F.12 – Navegadores
- **Descrição:** O sistema deve ser compatível com os navegadores Chrome, Firefox, Edge e Safari nas versões mais recentes.
- **Medição:** Testes de navegação em cada navegador suportado.
- **Usuários:** Todos os níveis de usuário

### R.N.F.13 – Dispositivos
- **Descrição:** O sistema deve ser responsivo, podendo ser usado em desktops, tablets e smartphones.
- **Medição:** Testes de layout responsivo em diferentes resoluções de tela.
- **Usuários:** Todos os níveis de usuário

### R.N.F.14 – Integração com APIs Externas
- **Descrição:** O sistema deve suportar integração com APIs externas de bancos e serviços financeiros.
- **Medição:** Testes de conexão, autenticação e troca de dados com APIs externas.
- **Usuários:** Todos os níveis de usuário

# 7. Diagrama de Caso de Uso

**7.1 Introdução**

O diagrama de caso de uso é uma ferramenta de modelagem que descreve o comportamento de um sistema a partir da perspectiva do usuário. Ele é usado para capturar os requisitos funcionais de um sistema.

- Especificam a visão externa do sistema.
- Descrevem como o sistema é percebido por seus usuários.
- Descrevem as interações entre os usuários e o sistema.

![Diagrama de Caso de Uso](img/dcu1.png "Diagrama de Caso de Uso")

**Os casos de uso:**
- Descrevem como os **usuários interagem com o sistema** (as funcionalidades do sistema)
- Facilitam a **organização dos requisitos** de um sistema.
- Dão uma **visão externa** do sistema
- O conjunto de casos de uso deve ser capaz de comunicar a **funcionalidade** e o **comportamento** do sistema para o cliente.
- Descrevem **o que** o sistema faz, mas **não** especificam **como** isso deve ser feito.

**7.2 Elementos do diagrama de caso de uso**

7.2.1 **Atores**

- Representam os papéis desempenhados por **elementos externos** ao sistema
  - Ex: humano (usuário), dispositivo de hardware ou outro sistema (cliente)
- Elementos que **interagem** com o sistema

Notação:

![Atores Notação](img/dcu_atores_notacao.png "Atores Notação")

**Exemplo: Loja de CDs**

**Identificando os atores**
- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja.
- A loja possui um **atendente** cuja função é atender os clientes durante a venda dos discos. A loja também possui um **gerente** cuja função é administrar o estoque para que não faltem discos. Além disso é ele quem dá folga ao atendente, ou seja, ele também atende os clientes durante a venda dos discos.

![Identificando os atores](img/dcu_identificando_atores.png "Identificando os atores")

**E o cliente?**
- Não é ator pois ele **não interage** com o sistema!

**7.2.2 Casos de uso**

- Representam **funcionalidades** do sistema (requisitos funcionais).
- São iniciados por **atores** ou por outros casos de uso.

> **Dica**: nomeie os casos de uso com **verbos** no **infinitivo**.

Notação:

![Casos de uso Notação](img/dcu_casos_de_uso_notacao.png "Casos de uso Notação")

**Exemplo: Loja de CDs**

**Identificando os casos de uso**

- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja. A loja possui um atendente cuja função é atender os clientes durante a **venda dos discos**.
- A loja também possui um gerente cuja função é **administrar o estoque** para que não faltem discos. Além disso é ele quem dá folga ao atendente, ou seja, ele também atende os clientes durante a **venda dos discos**.

![Identificando os casos de uso](img/dcu_identificando_casos_de_uso.png "Identificando os casos de uso")

**7.2.3 Relacionamentos**

**7.2.3.1 Relacionamento de associação**

- Indica que um ator **participa** de um caso de uso, ou seja, o ator **interage** (comunica-se) com o caso de uso.
- É representado por uma **linha sólida**.
- Um ator pode se relacionar com **um ou mais casos de uso**.

> Dicas:
> - Não use setas nas linhas de associação.
> - Associações não representam fluxo de informação.

![Relacionamento de associação](img/dcu_relacionamento_de_associacao.png "Relacionamento de associação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de associação**

- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja. A loja possui um _atendente_ cuja função é atender os clientes durante a **venda dos discos**.
- A loja também possui um _gerente_ cuja função é **administrar o estoque** para que não faltem discos. Além disso é ele quem dá folga ao _atendente_, ou seja, ele também atende os clientes durante a **venda dos discos**.

![Identificando os relacionamentos de associação](img/dcu_identificando_relacionamentos_de_associacao.png "Identificando os relacionamentos de associação")

**7.2.3.2 Relacionamento de generalização/especialização**

**Generalização de atores**

- Quando dois ou mais atores podem se **comunicar com o mesmo conjunto de casos de uso**.
- Indica que um ator **herda** as características de outro ator.
– Um filho (herdeiro) pode se comunicar com todos os casos de uso que seu pai se comunica.

> **Dica:** coloque os herdeiros **embaixo**.

**Notação:**

![Relacionamento de generalização/especialização de atores - notação](img/dcu_relacionamento_de_generalizacao_especializacao_notacao_de_atores.png "Relacionamento de generalização/especialização de atores - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de generalização/especialização de atores**

![Identificando os relacionamentos de generalização/especialização de atores](img/dcu_identificando_relacionamentos_de_generalizacao_especializacao_de_atores.png "Identificando os relacionamentos de generalização/especialização de atores")

**Generalização de casos de uso**

– O caso de uso filho herda o comportamento e o significado do caso de uso pai.
– O caso de uso filho pode incluir ou sobrescrever o comportamento do caso de uso pai.
– O caso de uso filho pode substituir o caso de uso pai em qualquer lugar que ele apareça.

> **Dica:** deve ser aplicada quando uma condição resulta na definição de
diversos fluxos alternativos.

Notação:

![Relacionamento de generalização/especialização de casos de uso - notação](img/dcu_relacionamento_de_generalizacao_especializacao_notacao_de_casos_de_uso.png "Relacionamento de generalização/especialização de casos de uso - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de generalização/especialização de casos de uso**

**Novos requisitos:**

- As vendas podem ser **à vista** ou **a prazo**. Em ambos os casos o estoque é
atualizado e uma nota fiscal, entregue ao consumidor.
- No caso de uma **venda à vista**, clientes cadastrados na loja e que compram mais de 5 CDs de uma só vez ganham um desconto de 1% para cada ano de cadastro.
- No caso de uma **venda a prazo**, ela pode ser parcelada em 2 pagamentos com um
acréscimo de 20%. As vendas a prazo podem ser pagas no **cartão** ou no **boleto**.
  - Para pagamento com **boleto**, são gerados boletos bancários que são entregues ao cliente e armazenados no sistema para lançamento posterior no caixa.
  - Para pagamento com **cartão**, os clientes com mais de 10 anos de cadastro na loja ganham o mesmo desconto das compras à vista.

![Identificando os relacionamentos de generalização/especialização de casos de uso](img/dcu_identificando_relacionamentos_de_generalizacao_especializacao_de_casos_de_uso.png "Identificando os relacionamentos de generalização/especialização de casos de uso")

**Identificando mais relacionamentos de generalização/especialização de casos de uso**

![Identificando mais relacionamentos de generalização/especialização de casos de uso](img/dcu_identificando_mais_relacionamentos_de_generalizacao_especializacao_de_casos_de_uso.png "Identificando mais relacionamentos de generalização/especialização de casos de uso")

**7.2.3.3 Relacionamento de dependência**

**Extensão**

- Representa uma variação/extensão do comportamento do caso de uso base.
- O caso de uso estendido só é executado sob certas circunstâncias.
- Separa partes obrigatórias de partes opcionais.
  - Partes obrigatórias: caso de uso base.
  - Partes opcionais: caso de uso estendido.
- Fatorar comportamentos variantes do sistema (podendo reusar este comportamento
em outros casos de uso).

**Notação:**

![Relacionamento de dependência (extensão) - notação](img/dcu_relacionamento_de_dependencia_extensao_notacao.png "Relacionamento de dependência (extensão) - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de dependência (extensão)**

**Novos requisitos:**
- No caso de uma venda à vista, clientes cadastrados na loja e que compram mais
de 5 CDs de uma só vez ganham um **desconto** de 1% para cada ano de cadastro.
- No caso de uma venda a prazo...
  - ...Para pagamento com cartão, os clientes com mais de 10 anos de cadastro na loja ganham o mesmo **desconto** das compras à vista.

![Identificando os relacionamentos de dependência (extensão)](img/dcu_identificando_relacionamentos_de_dependencia_extensao.png "Identificando os relacionamentos de dependência (extensão)")

**Inclusão**

- Evita repetição ao fatorar uma atividade
comum a dois ou mais casos de uso.
- Um caso de uso pode incluir vários casos de uso.

**Notação:**

![Relacionamento de dependência (inclusão) - notação](img/dcu_relacionamento_de_dependencia_inclusao_notacao.png "Relacionamento de dependência (inclusão) - notação")

**Exemplo: Loja de CDs**

**Novos requisitos:**
Para efetuar vendas ou administrar estoque, atendentes e gerentes terão que **validar** suas respectivas senhas de
acesso ao sistema.

![Identificando os relacionamentos de dependência (inclusão)](img/dcu_identificando_relacionamentos_de_dependencia_inclusao.png "Identificando os relacionamentos de dependência (inclusão)")

**7.2.4 Fronteira do sistema**

- Elemento opcional (mas essencial para um bom
entendimento).
- Serve para definir a área de atuação do sistema, ou seja, seus limites.

**Identificando a fronteira do sistema**

![Identificando a fronteira do sistema](img/dcu_identificando_a_fronteira_do_sistema.png "Identificando a fronteira do sistema")

---



