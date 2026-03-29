# Support Tickets API

## Português (pt-br)

### Descrição

Este projeto é uma API REST simples para gerenciamento de tickets de suporte. Permite criar, ler, atualizar e excluir tickets, além de atualizar seu status. Os dados são armazenados em um arquivo JSON, tornando-o uma solução leve para aplicações em pequena escala ou protótipos.

### Tecnologias Utilizadas

- **Node.js**: Ambiente de execução JavaScript para construir o servidor usando o módulo http nativo.
- **JSON**: Usado como um banco de dados simples para armazenar dados de tickets.
- **Middlewares Personalizados**: Para lidar com análise de JSON e roteamento de requisições.

### Pré-requisitos

- Node.js (versão 18 ou superior, para suporte ao modo watch)

### Instalação

1. Clone o repositório:

   ```
   git clone <url-do-repositório>
   cd support-tickets
   ```

2. Inicie o servidor:
   ```
   npm run dev
   ```

O servidor será executado em `http://localhost:3333` por padrão.

### Uso

Use ferramentas como Postman ou curl para interagir com os endpoints da API.

#### Endpoints da API

- `GET /tickets` - Recuperar todos os tickets
- `GET /tickets/:id` - Recuperar um ticket específico por ID
- `POST /tickets` - Criar um novo ticket
- `PUT /tickets/:id` - Atualizar um ticket
- `DELETE /tickets/:id` - Excluir um ticket
- `PATCH /tickets/:id/close` - Fechar um ticket (atualizar status para fechado)

Exemplo de requisição:

```
POST /tickets
Content-Type: application/json

{
  "title": "Problema com login",
  "description": "Usuário não consegue fazer login",
  "status": "open"
}
```

### Estrutura do Projeto

- `src/server.js`: Arquivo principal do servidor
- `src/controllers/tickets/`: Controladores para operações de tickets
- `src/database/`: Configuração do banco de dados e arquivo JSON
- `src/middlewares/`: Middlewares personalizados para JSON e roteamento
- `src/routes/`: Definições de rotas
- `src/utils/`: Funções utilitárias para análise

---

## English

### Description

This project is a simple REST API for managing support tickets. It allows creating, reading, updating, and deleting tickets, as well as updating their status. The data is stored in a JSON file, making it a lightweight solution for small-scale applications or prototypes.

### Technologies Used

- **Node.js**: JavaScript runtime for building the server using the native http module.
- **JSON**: Used as a simple database for storing ticket data.
- **Custom Middlewares**: For handling JSON parsing and request routing.

### Prerequisites

- Node.js (version 18 or higher, for watch mode support)

### Installation

1. Clone the repository:

   ```
   git clone <repository-url>
   cd support-tickets
   ```

2. Start the server:
   ```
   npm run dev
   ```

The server will run on `http://localhost:3333` by default.

### Usage

Use tools like Postman or curl to interact with the API endpoints.

#### API Endpoints

- `GET /tickets` - Retrieve all tickets
- `GET /tickets/:id` - Retrieve a specific ticket by ID
- `POST /tickets` - Create a new ticket
- `PUT /tickets/:id` - Update a ticket
- `DELETE /tickets/:id` - Delete a ticket
- `PATCH /tickets/:id/close` - Close a ticket (update status to closed)

Example request:

```
POST /tickets
Content-Type: application/json

{
  "title": "Issue with login",
  "description": "User cannot log in",
  "status": "open"
}
```

### Project Structure

- `src/server.js`: Main server file
- `src/controllers/tickets/`: Controllers for ticket operations
- `src/database/`: Database setup and JSON file
- `src/middlewares/`: Custom middlewares for JSON and routing
- `src/routes/`: Route definitions
- `src/utils/`: Utility functions for parsing
