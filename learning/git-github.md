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

## Git log

Objetivo|Comando|Comentários
-|-|-
Observar histórico de commits|`git log`|
Observar histórico de commits utiliznado uma linha cada|`git log --oneline`
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5MTc3MDg2MzgsNzg5MTU0OTg3LC0xOT
c4NzUyOTM0LC0xODAxNjMwMDMyLDk2MzI1NjgyOSwtMTk0MTQ5
NTczMywtODUyODE2ODY5LDIwNzQyNTg4NTksMjA4NTM2ODc4OV
19
-->