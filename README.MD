# bradesco-bank-system

## desenvolvedores

Pedro Henrique de Sá Gomes - RA: 12524232477 

Felipe de Ornelas Chaves - RA: 12525178266



## Resumo do Projeto

O `bradesco-bank-system` é uma aplicação backend desenvolvida em Spring Boot, projetada para simular um
sistema bancário. Ele gerencia contas, transações, usuários e inclui um serviço de notificação de fraudes.




## Pré-requisitos

Para rodar este projeto, você precisará ter instalado em sua máquina:

- **Java Development Kit (JDK) 17 ou superior**: Necessário para compilar e executar aplicações Java.
- **Docker Desktop**: Plataforma para desenvolver, enviar e executar aplicações em contêineres.
- **Plugin Lombok**: Para desenvolvimento da aplicação, é necessário ter o plugin do lombok instalado.

## Como Rodar o banco de dados com Docker Compose

Para iniciar  o banco de dados PostgreSQL usando Docker Compose, siga os passos abaixo:

1. Certifique-se de ter o Docker Desktop instalados e em execução.

2. Abra o terminal na pasta do projeto e execute o comando:

```bash
docker-compose up --build
```

Isso irá iniciar o contêiner do banco de dados.

Com o banco de dados em execução, você pode rodar a aplicação Spring Boot.

## Endpoints da API

Assumindo uma arquitetura RESTful e com base nos nomes dos serviços e controladores identificados no JAR, os seguintes endpoints podem estar disponíveis:

- **Usuários:**
    - `POST /api/users`: Criar um novo usuário.
    - `GET /api/users/{id}`: Obter detalhes de um usuário específico.
    - `PUT /api/users/{id}`: Atualizar informações de um usuário.
    - `DELETE /api/users/{id}`: Deletar um usuário.

- **Contas:**
    - `POST /api/accounts`: Criar uma nova conta.
    - `GET /api/accounts/{id}`: Obter detalhes de uma conta específica.
    - `GET /api/accounts/user/{userId}`: Obter contas de um usuário.

- **Transações:**
    - `POST /api/transactions/deposit`: Realizar um depósito.
    - `POST /api/transactions/withdraw`: Realizar um saque.
    - `POST /api/transactions/transfer`: Realizar uma transferência.
    - `GET /api/transactions/account/{accountId}`: Obter histórico de transações de uma conta.

- **Notificação de Fraudes:**
    - `POST /api/fraud-notifier/notify`: Enviar notificação de fraude (uso interno/webhook).
