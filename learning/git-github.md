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
Criar nova branch e alterar para ela|`git checkout -b nome-da-branch`|
Fazer merge|`git merge nome-da-branch`|Mover-se antes para a branch base
Fazer rebase|`git rebase nome-da-feature`|Mover-se antes para a branch base
Retirar as alterações que não foram _commitadas_|`git reset --hard`|
Retirar as alterações que não foram _commitadas_|`git restore <nome do arquivo>`|
Retirar as alterações que foram para _Staged Area_|`git restore --staged <nome do arquivo>`|
Retirar as alterações que sofreram _commit_|`git revert <sha-1>`|Use `:x` para salvar
Salvar alterações temporariamente|`git stash`|
Pegar stash para dar continuidade|`git stash pop`|Pega o primeiro stash da lista

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
eyJoaXN0b3J5IjpbLTE5NjIzMDgxMDksMTk2NjExMTA2Myw1Nz
c0OTUzODcsLTIwNDU1NTU3OCwtNzI5NTc1MTk4LDE0MzMzNjA4
NjMsNzY3MjkzMjc0LC02Njc1MzczNDcsNzg5MTU0OTg3LC0xOT
c4NzUyOTM0LC0xODAxNjMwMDMyLDk2MzI1NjgyOSwtMTk0MTQ5
NTczMywtODUyODE2ODY5LDIwNzQyNTg4NTksMjA4NTM2ODc4OV
19
-->