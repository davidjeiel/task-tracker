# Task Tracker

Este é um repositório para um aplicativo de rastreamento de tarefas. O aplicativo permite que os usuários acompanhem suas tarefas diárias, estabeleçam prazos, adicionem notas e marquem as tarefas como concluídas.

## Funcionalidades

- Adicionar uma nova tarefa com título, descrição e data de vencimento.
- Visualizar uma lista de todas as tarefas, incluindo as concluídas.

## Tecnologias utilizadas

- HTML5, CSS3 e VUE3 para o desenvolvimento do front-end.

## Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas em seu sistema:

- Node.js (versão 12 ou superior)

## Configuração

1. Clone este repositório em sua máquina local:

   ```bash
   git clone https://github.com/davidjeiel/task-tracker.git
   ```

2. Acesse o diretório do projeto:

   ```bash
   cd task-tracker
   ```

3. Instale as dependências do projeto:

   ```bash
   npm install
   ```

4. Copie o arquivo `.env.example` para `.env` e atualize as variáveis de ambiente, se necessário.

5. Inicie o servidor de desenvolvimento:

   ```bash
   npm start
   ```

6. Abra o navegador e acesse `http://localhost:3000` para usar o aplicativo Task Tracker.

## Uso

Ao acessar o aplicativo Task Tracker, você será apresentado à interface principal, onde poderá visualizar todas as tarefas cadastradas. Use os recursos disponíveis para gerenciar suas tarefas:

- Para adicionar uma nova tarefa, clique no botão "Adicionar Tarefa" e preencha os detalhes necessários.
- Para marcar uma tarefa como concluída, clique no botão de marcação ao lado da tarefa.
- Para editar uma tarefa existente, clique no botão "Editar" ao lado da tarefa e atualize os detalhes conforme necessário.
- Para excluir uma tarefa, clique no botão "Excluir" ao lado da tarefa.
- Use os filtros e opções de classificação para personalizar a exibição das tarefas.

## Contribuição

Contribuições são bem-vindas! Se você quiser melhorar este projeto, siga as etapas abaixo:

1. Faça um fork deste repositório.
2. Crie um branch para sua nova funcionalidade ou correção de bug:
   ```bash
   git checkout -b feature/nova-funcionalidade
   ```
   ou
   ```bash
   git checkout -b bugfix/correcao
   ```
3. Faça as alterações desejadas e adicione os arquivos modificados:
   ```bash
   git add .
   ```
4. Faça um commit das alterações:
   ```bash
   git commit -m "Descrição das alterações"
   ```
5. Envie as alterações para o repositório remoto:
   ```bash
   git push origin nome-da-branch
   ```
6. Abra uma pull request no repositório original.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
