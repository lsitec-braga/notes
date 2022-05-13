# Git e GitHub

## Instalação

- [Git for windows](https://git-scm.com/)

## Conceitos teóricos

-   `HEAD`: Estado atual do nosso código, ou seja, onde o Git os colocou
-   `Working tree`: Local onde os arquivos realmente estão sendo armazenados e editados
-   `index`: Local onde o Git armazena o que será  _commitado_, ou seja, o local entre a  _working tree_  e o repositório Git em si.

## Ciclo de vida dos arquivos com git

![The lifecycle of the status of your files.](https://git-scm.com/book/en/v2/images/lifecycle.png)

## Configuração do git

```bash
# Configs genéricas
git config --global user.name "Seu nome do github aqui"
git config --global user.email "seu@emailDoGithub.aqui"

# Minhas configs
git config --global user.name "lsitec-braga"
git config --global user.email "diego.braga@lsitec.org.br"
```

## Comandos básicos

Objetivo|Comando|Comentários
-|-|-
Criar um repositório|`git init`|
Analisar estado do repositório|`git status`|
Adicionar arquivos da pasta atual ao *track* do git|`git add .`|
Fazer commit|`git commit -m "Mensagem do commit"`|Recomenda-se adicionar uma mensagem descritiva do commit|
Observar histórico de commits|`git log`|O mais recente é o que aparece primeiro
Adicionar mudanças da origin para o repositório local|`git pull origin main`|
Alterar branch|`git checkout nome-da-branch`|
Criar uma branch|`git branch nome-da-branch`|
Renomear _branch_|`git branch -M main`|
Criar nova branch e alterar para ela|`git checkout -b nome-da-branch`|
Fazer merge|`git merge nome-da-branch`|Mover-se antes para a branch base
Fazer rebase|`git rebase nome-da-feature`|Mover-se antes para a branch base
Retirar as alterações que não foram _commitadas_|`git reset --hard`|
Retirar as alterações que não foram _commitadas_|`git restore <nome do arquivo>`|
Retirar as alterações que foram para _Staged Area_|`git restore --staged <nome do arquivo>`|
Retirar as alterações que sofreram _commit_|`git revert <sha-1>`|Use `:x` para salvar
Salvar alterações temporariamente|`git stash`|
Listar alterações temporariamente|`git stash list`|
Aplicar alterações da stash definida|`git stash apply <number>`|
Remover alterações da stash list|`git stash drop <number>`|
Pegar stash para dar continuidade|`git stash pop`|Pegar o último stash da lista
Conferir alterações feitas|`git diff`
Definir tag no commit|`git tag -a v0.1.0 -m "Lançando a versão beta do aplicativo"`|
Listar tags|`git tag`|
Mover commit específico para outra branch|`git cherry-pic <hash-commit>`|
Descobrir commit de uma alteração|`git bisect start`|
Saber quem fez alteração em cada linha de código|`git blame`

## Merge vs Rebase

[Entendendo melhor Merge vs Rebase](https://medium.datadriveninvestor.com/git-rebase-vs-merge-cc5199edd77c)

## Git log

Links úteis

- [Outras maneiras de organizar os histporicos do git](https://devhints.io/git-log)
- [Parâmetros do git log](https://devhints.io/git-log-format)

Objetivo|Comando|Comentários
-|-|-
Observar histórico de commits|`git log`|
Enxuto em uma linha cada|`git log --oneline`|
Com detalhes das alterações|`git log -p`

## Git ignore

Arquivo `.gitignore`

```
arquivo-a-ser-ignorado.ext
pasta-a-ser-ignorada/
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwNTM0ODIxMjUsLTEyMDk1NzI4MTcsNz
Y4OTgzMTksLTM2NDUwMDIxMSwzMDEyNTY0MjQsLTcyMzI1NzEz
MiwxNjQwNzI5NjUwLDE2NTY4NTEzOTYsLTE5NjIzMDgxMDksMT
k2NjExMTA2Myw1Nzc0OTUzODcsLTIwNDU1NTU3OCwtNzI5NTc1
MTk4LDE0MzMzNjA4NjMsNzY3MjkzMjc0LC02Njc1MzczNDcsNz
g5MTU0OTg3LC0xOTc4NzUyOTM0LC0xODAxNjMwMDMyLDk2MzI1
NjgyOV19
-->