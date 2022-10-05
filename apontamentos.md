# Apontamentos - Servidor

## Requisitos

- Instalar [Node.JS](https://nodejs.org/en/download/)
- Instalar [Postgres](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)

## Iniciar Postgres (Banco de dados)

1. Rode o executável do Postgres
2. Siga o passo a passo da instalação preenchendo os campos necessários
3. Adicione o caminho `C:\Program Files\PostgreSQL\14\bin` às variáveis do sistema
4. Insira o seguinte comando `psql -U postgres` (postgres é o nome do usuário)
5. Insira a senha do servidor que foi cadastrado na etapa de instalação
6. Agora com o servidor postgres ligado, siga o passo a passo para iniciar o servidor local

## Rodar servidor local

1.  Ir até o diretório `/server`
2.  Aplicar o comando  `npm install`
3.  Instalar o banco de dados (Seguir tutorial acima)
4.  Criar um banco, senha e usuário de testes com os devidos privilégios (Seguir tutorial acima)
5.  No diretório `server` editar o template do arquivo `example.env` com as credenciais criadas no PostgreSQL
6. Renomear o `example.env` para `.env`
7.  No diretório `server` aplicar o comando  `npx prisma migrate dev`. Uma mensagem deve mostrar que o banco foi gerado com sucesso
8.  Ir para o diretório `/src`
9.  Aplicar o comando `node server.js`
10.  Instalar o aplicativo [Postman](https://dl.pstmn.io/download/latest/win64)
11.  Importar a collection no postman que está no diretório `/server/tests`
12.  Realizar requisições para api

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc5Njk4MDMzNCwtMzY5MDg2OTg2LDE5Nj
MyMTI0MDAsLTE1MTM2NzAzNiwtMjEzNDAzMzk2MCw0NDQ3NDIz
NzQsMTMxMzU4NjcxNCwtMTIyNzk4NjA4NF19
-->