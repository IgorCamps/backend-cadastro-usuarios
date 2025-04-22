# Backend de Cadastro de Usuários

API RESTful para cadastro básico de usuários com **Node.js + Express + MongoDB**.

## 🛠️ Tecnologias
- **Node.js** (v18+)
- **Express** (Framework web)
- **MongoDB Atlas** (Banco de dados na nuvem)

## Como Executar

### Pré-requisitos
- Node.js instalado
- MongoDB Atlas ou local
- Git (opcional)

### Passo a Passo
1. Clone o repositório:
   ```bash
   git clone https://github.com/IgorCamps/backend-cadastro-usuarios.git
   cd backend-cadastro-usuarios

2. Instale as dependências
   ```bash
   npm install || npm i
   ```
3. Crie o arquivo .env na raiz (use o .env.example como base):
   ```bash
   DATABASE_URL="mongodb+srv://Igor:5RsUJT6goxhiuRe3@cluster0.rqpr0.mongodb.net/Users?retryWrites=true&w=majority&appName=Cluster0"
   ```

4. Inicie o servidor:
     ```bash
     node server.js || node --watch server.js
     ```
# Endpoints da API
POST `/usuarios ` - Cadastra novo usuário
Request:

```json
  {
  "name": "Fulano da Silva",
  "email": "fulano@exemplo.com",
  "age": "18"
  }
```
Response (201 Created):
```json
  {
  "name": "Fulano da Silva",
  "email": fulano@exemplo.com,
  "age": "18"
  }
```
GET `/usuarios` - Lista todos usuários
Response (200 OK):
```json
[
  {
    "name": "Fulano da Silva",
    "email": fulano@exemplo.com,
    "age": "18"
  }
]
```
PUT `/usuarios/:id` - Atualiza um usuário

**Parâmetro URL:**
- `id` (string): ID do usuário a ser atualizado

```json
  {
    "name": "Fulano dos Santos",
    "email": fulano@exemplo.com,
    "age": "20"
  }
```

Response (201 Ok) - 'Usuário atualizado com sucesso!'

DELETE `/usuarios/:id` - Remove um usuário
Parâmetro URL:
- `id` (string): ID do usuário a ser deletado

Response (200 OK):
```json
{
  "message": "Usuário deletado com sucesso!"
}
```
