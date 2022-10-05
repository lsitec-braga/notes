# Apontamentos - Servidor

## Requisitos

- [Node.JS](https://nodejs.org/en/download/)
- [Postgres](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)

## Iniciar Postgres

1. Rode o executável do Postgres
2. Siga o passo a passo da instalação preenchendo os campos necessários
3. Adicione o caminho `C:\Program Files\PostgreSQL\14\bin` às variáveis do sistema
4. Insira o seguinte comando `psql -U postgres`
5. Insira a senha do servidor
6. Agora com o servidor postgres ligado, na pasta raiz do projeto, insira o comando `node server/src/server.js`

## Rodar servidor local

1.  Ir até o diretório /server
2.  Aplicar o comando  `npm install`
3.  Instalar o banco de dados
4.  Criar um banco, senha e usuário de testes com os devidos privilégios No diretório server editar o template arquivo example.env com as credenciais criadas no PostgreSQL Renomear o example.env para .env
5.  No diretório server aplicar o comando  `npx prisma migrate dev`. Uma mensagem deve mostrar que o banco foi gerado com sucesso image
6.  Ir para o diretório /src
7.  Aplicar o comando  `node server.js`
8.  Instalar o aplicativo  [Postman](https://dl.pstmn.io/download/latest/win64)
9.  Importar a collection no postman que está no diretório /server/tests
10.  Realizar requisições para api

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1MTM2NzAzNiwtMjEzNDAzMzk2MCw0ND
Q3NDIzNzQsMTMxMzU4NjcxNCwtMTIyNzk4NjA4NF19
-->