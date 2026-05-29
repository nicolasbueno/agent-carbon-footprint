# Agente Organizador de Tarefas com Python e Trello

## Sobre o Projeto

Este projeto foi desenvolvido como parte do desafio **"Criando um Agente para Automatizar um Fluxo de Trabalho em Python"**, da DIO.

A proposta do desafio é criar e configurar um agente capaz de interagir com o Trello para apoiar a organização e automação de tarefas. O projeto simula um cenário real de produtividade, onde tarefas podem ser criadas, listadas e movimentadas entre listas de um quadro Kanban de forma automatizada.

O objetivo principal é demonstrar como Python pode ser utilizado para integrar sistemas externos por meio de APIs, reduzindo atividades manuais e tornando o fluxo de trabalho mais eficiente.

## Objetivo

Construir um agente em Python integrado ao Trello, capaz de automatizar etapas de um fluxo de trabalho baseado em tarefas.

Entre as principais funcionalidades trabalhadas estão:

- Configuração de ambiente virtual em Python
- Integração com a API do Trello
- Registro e autorização de aplicação no Trello
- Criação de tarefas em um quadro
- Listagem de tarefas existentes
- Movimentação de cards entre listas
- Organização do fluxo em formato Kanban

## Tecnologias Utilizadas

- Python
- Trello API
- Requests
- Dotenv
- Git e GitHub
- Ambiente virtual com venv

## Estrutura do Projeto

```text
agent-carbon-footprint/
├── agents/
│   └── agent04/
│       ├── agenttaskmanager/
│       ├── readme.md
│       └── requirements.txt
├── readme.md
└── demais arquivos do repositório
```

## Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/agent-carbon-footprint.git
```

Acesse a pasta do projeto:

```bash
cd agent-carbon-footprint
```

### 2. Acesse a pasta do desafio

```bash
cd agents/agent04
```

### 3. Crie o ambiente virtual

```bash
python -m venv .venv
```

### 4. Ative o ambiente virtual

No Windows:

```bash
.venv\Scripts\activate
```

No Linux/Mac:

```bash
source .venv/bin/activate
```

### 5. Instale as dependências

```bash
pip install -r requirements.txt
```

Caso o projeto não possua todas as dependências no arquivo `requirements.txt`, instale manualmente as bibliotecas utilizadas:

```bash
pip install requests python-dotenv
```

## Configuração das Credenciais do Trello

Para que o agente consiga se comunicar com o Trello, é necessário configurar as credenciais da API.

Crie um arquivo `.env` na pasta do projeto, seguindo o exemplo abaixo:

```env
TRELLO_API_KEY=sua_api_key
TRELLO_TOKEN=seu_token
TRELLO_BOARD_ID=id_do_quadro
```

> Importante: nunca publique chaves, tokens ou credenciais reais no GitHub.

Caso exista um arquivo `.env.exemplo` no projeto, ele pode ser usado como referência para criar o arquivo `.env` real.

## Como Obter as Credenciais do Trello

Para registrar e autorizar o uso da API do Trello:

1. Acesse a área de desenvolvedor do Trello.
2. Gere sua chave de API.
3. Autorize o uso da aplicação para obter o token.
4. Identifique o ID do quadro que será utilizado pelo agente.
5. Configure essas informações no arquivo `.env`.

Essas credenciais permitem que o agente consulte quadros, listas e cards, além de executar ações automatizadas no Trello.

## Execução do Agente

Após configurar o ambiente e as credenciais, execute o script principal do agente.

Exemplo:

```bash
python agenttaskmanager/agent.py
```

> O nome ou caminho do arquivo principal pode variar conforme a estrutura do projeto. Caso necessário, valide o arquivo correto dentro da pasta `agent04`.

## Fluxo de Funcionamento

O agente funciona como uma camada de automação entre o usuário e o Trello.

O fluxo esperado é:

1. O usuário configura suas credenciais da API do Trello.
2. O agente se conecta ao quadro informado.
3. As listas e tarefas são consultadas.
4. O agente executa ações como criação, listagem ou movimentação de cards.
5. O Trello é atualizado automaticamente com base nas ações realizadas.

## Exemplo de Uso

Um possível cenário de uso seria:

- Criar uma tarefa na lista "A Fazer"
- Consultar todas as tarefas pendentes
- Mover uma tarefa para "Em Andamento"
- Finalizar a tarefa movendo o card para "Concluído"

Esse tipo de automação pode ser aplicado em rotinas de estudo, gestão de pequenas demandas, acompanhamento de atividades operacionais ou organização pessoal.

## Aprendizados

Durante o desenvolvimento deste projeto, foram praticados conceitos importantes como:

- Consumo de APIs REST com Python
- Uso de variáveis de ambiente para proteger credenciais
- Organização de projeto Python
- Automação de tarefas repetitivas
- Manipulação de dados retornados por APIs
- Versionamento de código com Git e GitHub
- Documentação técnica com Markdown

## Boas Práticas Aplicadas

- Separação de credenciais em arquivo `.env`
- Não exposição de tokens no repositório
- Uso de ambiente virtual para isolar dependências
- Organização do código por responsabilidade
- Documentação clara para reprodução do projeto
- Registro das etapas necessárias para instalação, configuração e execução

## Possíveis Melhorias Futuras

- Criar interface simples via terminal para interação com o agente
- Adicionar tratamento de erros mais detalhado
- Implementar logs de execução
- Permitir escolha dinâmica de quadro e listas
- Criar comandos personalizados para diferentes fluxos de trabalho
- Integrar o agente com outras ferramentas de produtividade

## Autor

Projeto desenvolvido por **Nicolas dos Santos Bueno** como parte do desafio da DIO.

LinkedIn: <https://www.linkedin.com/in/nicolasbueno-/>

## Créditos

Este projeto foi desenvolvido a partir do repositório-base disponibilizado pela DIO:

<https://github.com/digitalinnovationone/agent-carbon-footprint>
