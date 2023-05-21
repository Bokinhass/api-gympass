# App

GymPass style app.

## RFs (Requisitos funcionais)

- [x] Deve ser possível se cadastrar;

- [] Deve ser possível se autenticar;

- [] Deve ser possível obter o perfil de um usuário logado;

- [] Deve ser possível obter o número de check-ins realizados pelo usuário logado;

- [] Deve ser possível o usuário obter o seu histórico de check-ins;

- [] Deve ser possível o usuário buscar academias próximas (até 10km);

- [] Deve ser possível o usuário buscar academias pelo nome;

- [] Deve ser possível o usuário realizar check-in em uma academia;

- [] Deve ser possível validar o check-in de um usuário;

- [] Deve ser possível cadastrar uma academia;

## RNs (Regras de negócio)

- [x] O usuário não deve poder se cadastrar com um e-mail duplicado;

- [] O usuário não pode fazer 2 check-ins no mesmo dia;

- [] O usuário não pode fazer check-in se não estiver perto (100m) da academia;

- [] O check-in só pode ser validado até 20 minutos após ser criado;

- [] O check-in só pode ser validado por administradores;

- [] A academia só pode ser cadastrada por administradores;

## RNFs (Requisitos não-funcionais)

- [x] A senha do usuário precisa estar criptografada;

- [x] Os dados da aplicação precisam estar persistidos em um banco PostgreSQL;

- [] Todas listas de dados precisam estar paginadas com 20 itens por página;

- [] O usuário deve ser identificado por um JWT (JSON Web Token);

## Comandos

- docker run --name api-gympass-pg -e POSTGRESQL_USERNAME=docker -e POSTGRESQL_PASSWORD=docker -e POSTGRESQL_DATABASE=api-gympass -p 5432:5432 bitnami/postgresql

- docker start api-gympass-api-gympass-pg-1

- docker stop api-gympass-api-gympass-pg-1

- npm run dev

- npx prisma migrate dev

- npx prisma studio
