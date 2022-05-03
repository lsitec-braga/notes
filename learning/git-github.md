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
Adicionar mudanças da origin para o repositório local|`git pull origin main`|
Alterar branch|`git checkout nome-da-branch`|
Criar uma branch|`git branch nome-da-branch`|
Criar nova branch e alterar para ela|`git checkout -b nome-da-branch`|
Fazer merge|`git merge nome-da-branch`|
Fazer rebase|`git rebase`
Observar histórico de commits|`git log`|O mais recente é o que aparece primeiro

## Git Merge

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
eyJoaXN0b3J5IjpbNzY3MjkzMjc0LC02Njc1MzczNDcsNzg5MT
U0OTg3LC0xOTc4NzUyOTM0LC0xODAxNjMwMDMyLDk2MzI1Njgy
OSwtMTk0MTQ5NTczMywtODUyODE2ODY5LDIwNzQyNTg4NTksMj
A4NTM2ODc4OV19
-->