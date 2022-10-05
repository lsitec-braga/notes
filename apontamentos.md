# Apontamentos

## Requisitos

- Node.JS

## Rodar servidor local

1. Abra o terminal
2. Insira o seguinte comando 
```bash
psql -U postgres
```
3. Insira a senha do servidor
4. Agora com o servidor postgres ligado, na pasta raiz do projeto, insira o comando 
```bash
node server/src/server.js
```

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
eyJoaXN0b3J5IjpbLTEzNjg0MDQ0NDcsMTMxMzU4NjcxNCwtMT
IyNzk4NjA4NF19
-->