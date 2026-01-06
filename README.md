O Fórum Hub é uma aplicação back-end desenvolvida como parte do desafio do programa Oracle Next Education (ONE) em parceria com a Alura.
O objetivo do projeto é criar uma API REST responsável por gerenciar tópicos de discussão, simulando o funcionamento de um fórum online.

A aplicação permite que usuários autenticados criem, visualizem, editem e excluam tópicos, garantindo regras de segurança e controle de acesso.

Funcionalidades

Cadastro e autenticação de usuários

Geração de token JWT

Criação de tópicos

Listagem de tópicos

Detalhamento de tópico por ID

Atualização de tópico (somente pelo autor)

Exclusão de tópico (somente pelo autor)

Validação de dados

Controle de acesso por autenticação

Regras de Negócio

Apenas usuários autenticados podem criar, editar ou excluir tópicos.

Cada tópico pertence a um único usuário.

O usuário só pode alterar ou excluir seus próprios tópicos.

A data de criação do tópico é gerada automaticamente pelo sistema.

Endpoints protegidos exigem Bearer Token (JWT).

Autenticação

A autenticação é realizada via JWT (JSON Web Token).

Exemplo de Header:
Authorization: Bearer SEU_TOKEN_AQUI


O token é gerado após o login do usuário e deve ser enviado em todas as requisições protegidas.

Endpoints Principais
Criar Tópico

POST /topicos

{
  "titulo": "Dúvida sobre Java",
  "mensagem": "Não entendi herança",
  "curso": "Java"
}

 Listar Todos os Tópicos

GET /topicos

 Buscar Tópico por ID

GET /topicos/{id}

 Atualizar Tópico

PUT /topicos/{id}

{
  "titulo": "Dúvida resolvida",
  "mensagem": "Agora entendi herança",
  "curso": "Java"
}

 Excluir Tópico

DELETE /topicos/{id}

 Tecnologias Utilizadas

Java

Spring Boot

Spring Security

Spring Data JPA

JWT (JSON Web Token)

Banco de Dados (H2 ou MySQL)

Maven

Insomnia (para testes de API)

 Organização do Projeto

controller → Camada de controle das requisições

service → Regras de negócio

repository → Acesso ao banco de dados

model → Entidades

security → Configurações de autenticação e autorização

 Documentação e Organização

O projeto foi desenvolvido seguindo as orientações do Trello do desafio, que contém:

Backlog completo

Regras de negócio

Requisitos obrigatórios e extras

 Comunidade

A troca de conhecimento faz parte do processo!
Utilize o Discord do programa para:

Tirar dúvidas

Compartilhar soluções

Ajudar outros participantes

 Considerações Finais

Este projeto consolida conhecimentos importantes sobre:

APIs REST

Segurança com JWT

Boas práticas em aplicações Java

Organização e arquitetura de projetos backend

