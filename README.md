# API de Autenticação com Node.js, Express e MongoDB

Esta é uma API RESTful construída com Node.js e Express, utilizando MongoDB como banco de dados. Ela implementa um sistema básico de autenticação com JWT e bcrypt, contendo rotas públicas (cadastro e login) e rotas protegidas (acesso apenas com token válido).

## Tecnologias Utilizadas

- **Node.js** — Ambiente de execução JavaScript no backend.
- **Express** — Framework web para construção de APIs.
- **MongoDB** — Banco de dados NoSQL para armazenamento dos usuários.
- **JWT (jsonwebtoken)** — Geração e verificação de tokens de autenticação.
- **Bcrypt** — Criptografia segura de senhas.

## Funcionalidades

- Cadastro de usuários com senha criptografada.
- Login com verificação de credenciais e emissão de token JWT.
- Proteção de rotas privadas com middleware de autenticação.
- Listagem de usuários (rota protegida), com ocultação da senha.

## Estrutura do Projeto

POST /cadaster

{
  "name": "User",
  "email": "user@email.com",
  "password": "minhasenha"
}

POST /login

Autentica o usuário e retorna um token JWT.

{
  "email": "user@email.com",
  "password": "minhasenha"
}

Exemplo de Token gerado:
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5..."
}

ROTAS PRIVADAS:

GET /list-users
Requisição:
Authorization: Bearer SEU_TOKEN

Resposta:

{
  "message": "Usuarios listados com sucesso.",
  "users": [
    {
      "id": "123",
      "name": "User",
      "email": "user@email.com"
    }
  ]
}


## Considerações Finais

Este projeto foi desenvolvido com foco em aprendizado e prática de conceitos essenciais de backend, como autenticação, segurança e organização de rotas. Fique à vontade para explorar, testar e sugerir melhorias.

Obrigado por ler até aqui.



