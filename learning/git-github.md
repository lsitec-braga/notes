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
Enxuto em uma linha cada|`git log --oneline`|
Com detalhes das alterações|`git log -p`

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTcxNzY0MzY3Niw3ODkxNTQ5ODcsLTE5Nz
g3NTI5MzQsLTE4MDE2MzAwMzIsOTYzMjU2ODI5LC0xOTQxNDk1
NzMzLC04NTI4MTY4NjksMjA3NDI1ODg1OSwyMDg1MzY4Nzg5XX
0=
-->