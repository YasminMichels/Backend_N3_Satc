# Backend Projeto: API para Gerenciamento de Posts e Usuários

Este projeto fornece uma API para gerenciar usuários, autenticação e posts em uma plataforma. A API foi desenvolvida utilizando **Spring Boot** e expõe endpoints para criação, edição, exclusão e consulta de informações relacionadas a usuários e posts.

---

## Endpoints

### 1. Usuários
#### Criar novo usuário
- **URL:** `POST /user/novouser`
- **Exemplo de Body:**
  ```json
  {
    "idusuario": null,
    "nome": "João Silva",
    "telefone_celular": 55999887766,
    "email": "joao.silva@example.com",
    "senha": "senha123",
    "tipo_usuario": 1,
    "token": "abc123xyz"
  }
Login
URL: POST /auth/login
Exemplo de Body:
json
Copiar código
{
  "username": "joao.silva@example.com",
  "password": "senha123"
}
2. Posts
Criar ou Atualizar Post
URL: PUT /api/postcad/save
Exemplo de Body:
json
Copiar código
{
  "idpost": 0,
  "usuario": { "idusuario": 1 },
  "titulo": "tiaguinho",
  "nome_causa": "q",
  "filtro_animal": "Cachorro",
  "filtro_raca": "Vira-lata",
  "filtro_porte": "Médio",
  "filtro_causa": "Adoção",
  "descricao": "q",
  "chavepix": "22",
  "contato": "2",
  "status": 1
}
Buscar Post por ID
URL: GET /api/postcad/getpost/{id}
Exemplo de URL: GET /api/postcad/getpost/27
Listar Todos os Posts
URL: GET /api/postcad/list
Editar Post
URL: PUT /api/postcad/editpost
Exemplo de Body:
json
Copiar código
{
  "idpost": 17,
  "usuario": {
    "idusuario": 1,
    "nome": "João cachorro",
    "telefone_celular": 999999999,
    "email": "joao.silva@email.com",
    "senha": "senha123",
    "tipo_usuario": 1,
    "token": "token_exemplo"
  },
  "titulo": "titulo para pipipopopo do animal",
  "nome_causa": "auauau",
  "filtro_animal": "cachorro",
  "filtro_raca": "Vira-lata",
  "filtro_porte": "Médio",
  "filtro_causa": "Adoção",
  "descricao": "descrição sobre animal e o serviço/ação que esta sendo requisitado",
  "chavepix": "274052938570",
  "contato": "(99) 99999-9999",
  "status": 1,
  "imagem": null
}
Excluir Post
URL: DELETE /api/postcad/deletepost/{id}
Exemplo de URL: DELETE /api/postcad/deletepost/17
3. Transações
Criar Transação
URL: POST /transacoes
Exemplo de Body:
json
Copiar código
{
  "origem": "500-1",
  "destino": "320-2",
  "valor": 100
}
Configuração
Clone o repositório:

bash
Copiar código
git clone <URL-DO-REPOSITORIO>
cd <NOME-DO-REPOSITORIO>
Configure o ambiente:

Porta do Servidor: 8080
Banco de dados configurado em application.properties.
Inicie o servidor:

bash
Copiar código
./mvnw spring-boot:run
