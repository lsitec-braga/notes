# Atividades PO - dotA

## Links úteis

### Documentação

- [Drive Dota Público](https://drive.google.com/drive/folders/1El3wD3XIZfDskHNhqsmA-em18fU2ERw-)
- [Planilha Dota](https://docs.google.com/spreadsheets/d/1vYYiKfqUQ9IWmB7hvXE9hFXUomil17JVDZPd0AwVaeI/edit#gid=1690275737)
- [Documentação Dota](https://docs.google.com/document/d/1Nxw7SmU_juwZ-bb-b6BexMMARycb0FtNFS4UaKzPIWA/edit#heading=h.rhj9rwtufcy)

### Github

- [Repositório dota-web](https://github.com/lab-de-sistema-integraveis-tecnologico/dota-web)
- [Repositório dota-aws](https://github.com/lab-de-sistema-integraveis-tecnologico/dota-aws)
- [Repositório dota-configuration-server](https://github.com/lab-de-sistema-integraveis-tecnologico/dota-configuration-server)
- [Kanban Dota](https://github.com/orgs/lab-de-sistema-integraveis-tecnologico/projects/7)

### Sistema

- [Sistema antigo](https://sr.dota-iot.com.br/)
- [Sistema novo](https://dota-mobile.lsitec.org.br/)

### Infra

- [AWS](https://sa-east-1.console.aws.amazon.com/console/home?region=sa-east-1#)
- [Monitor AWS](https://sa-east-1.console.aws.amazon.com/cloudwatch/home?region=sa-east-1#dashboards:name=Monitora_Server_EC2)
- [Main Database](http://dota-mysql.mobile.lsitec.intranet/phpmyadmin/index.php)
- [Backup Database](https://dotabkp-mysql.mobile.lsitec.intranet/phpmyadmin/index.php)
- [Server de configuração](http://10.0.160.47:18083/#/login?to=/dashboard/overview)

## Assumindo projeto

Ao assumir o projeto, os seguintes pontos devem ser dominados:

- [ ] Entender o que se espera do produto para as próximas semanas, meses (visão do cliente/stakeholder)
- [x] Analisar Product Backlog
- [x] Analisar os custos do AWS
- [x] Analisar a plataforma do dota 1 (pegar acesso de admin com o Alexandre)
- [ ] Analisar a plataforma do dota 2
- [ ] Entender Infra do dota 1 (vou te passar um resumo e o acesso)
- [ ] Entender Infra do dota 2 (pedir acesso admin para o Alexandre)

## Tarefas diárias

- Enviar um resumo das atividades restantes para o Ickson
- Enviar um resumo no skype (no final do expediente) sobre o progresso da correção de bugs
- Após a daily, atualizar planilha do projeto de acordo com o que foi falado na daily e conferir o progresso das tasks
- Acompanhar o Welington nos testes e garantir que os bugfix foram executados (garantir a qualidade do produto)

Atual - Report issues

```
Report 18/01/2023
-----------------
TOTAL DE ISSUES: 67
Fechadas: 64
Abertas: 3, sendo 2 novas adicionadas hoje
> Em validação: 1
> Em desenvolvimento: 2
```

Atual - resumo atividades Ickson

```
, segue a lista resumida das atividades pendentes:
- Aguardar avaliação do teste de estresse para ver se ocorrerá problemas de performance na plataforma
- Correção de possíveis bugs reportados durante a reunião com a São Rafael
- Auxiliar na avaliação pós teste de estresse sobre a infra
```

Backup - Report issues

```
Report 10/01/2023
-----------------
TOTAL DE ISSUES: 48
Fechadas: 33
Abertas: 9, sendo 3 novas adicionadas hoje e 1 reabertas hoje
> Em validação: 3
> Em desenvolvimento: 12
Obs: 2 issues duplicadas, que estavam na contagem total de issues, foram desconsideradas da contagem
```

Backup - resumo atividades Ickson

```
Ickson, segue a lista resumida das atividades pendentes:
- Corrigir Bugs: #31, #40, #52, #57, #59, #64, #65, #68, #69, #70, #71
- Fazer itens de qualidade de vida: #66
- Fazer script para o teste de estresse
- Auxiliar na avaliação pós teste de estresse sobre a infra.
```



## Pontos de teste

- [ ] Painel de controle
- [ ] Ativar alarmes
- [ ] Tratar alarmes
- [ ] gráficos, (ontem a gente viu que só tinha pontos no gráfico, sem linhas)
- [ ] gráfico de porta,
- [ ] filtros de estado junto como os filtros de empresa (pelo que eu vi tem problemas nesses filtros)
- [ ] ver se os sensores estão aparecendo corretamente,
- [ ] histórico de alarmes,
- [ ] ver se o card novo apresenta corretamente múltiplos alarmes (temperatura, porta, tensão e pânico ao mesmo tempo)
- [ ] Consulta de informações adicionais da tratativa de alarme

## Funcionalidades Dota1 = Dota2

Garantir que as seguintes funcionalidades funcionem no Dota 2 por funcionarem no Dota 1:

- [ ] Conexão com os dotAs
- [ ] Painel de controle
- [ ] Gerenciamento e conexão com os pontos
- [ ] Filtragem de pontos
- [ ] Gerenciamento de empresas
- [ ] Ativação e tratamento de alarmes
- [ ] Geração dos gráficos dentro do painel de controle
- [ ] Filtragem dos dados dentro dos gráficos que serão gerados
- [ ] Visualização dos gráficos de todos os sensores (temperatura, porta, tensão, pânico)
- [ ] Download dos dados gerados nos gráficos
- [ ] Perfis de usuários

## Acordo com o Ickson

Ickson, seguem as atividades para conclusão:
1. Resolver issues que foram/estão sendo reportadas no github (As novas issues criadas são referentes à bugs encontrados no sistema, performance e funcionalidades que não estão tendo o comportamento esperado de acordo com o documento de requisitos)
2. Ajustes simples para melhorar a qualidade de vida do sistema
	2.1. Botão de filtrar por período disponível sem a necessidade de expandir o ponto no painel de controle
	2.2. Tooltip ao deixar o mouse em cima dos botões presentes nos cards dos pontos no painel de controle
	2.3. Manter o mesmo padrão de cores da legenda dos gráficos
	2.4. O ponto que estiver sem conexão nos últimos dias, ao ser expandido, deve apresentar gráficos de seus sensores, mesmo que vazio. Além disso, deve ser possível a filtragem de dados por período, para resgatar dados enquanto havia conexão
3. Auxiliar na avaliação pós teste de estresse sobre a infra.

## Marcos dotA

10/01 - Testes gerais na plataforma e confirmar correção dos bugs reportados anteriormente
11/01 - Dia do Teste de estresse
12/01 - Avaliação dos resultados do teste de estresse

16/01 - Validação das features utilizadas que possam afetar a SR ou experiência do usuário
17/01 - Preparação para a apresentação
18/01 - Apresentação da interface para São Rafael
19/01 - Início dos testes de migração de dados do dotA1 para o dotA2
20/01 - Fim dos testes de migração de dados do dotA1 para o dotA2

23/01 - Preparação para a Review
24/01 - Review dotA2 - Sprint3

## Atividades


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQwOTk4ODA1NywxNjQ1MjAzMzg1LDE1Mz
UwMTE0NiwxMDkyMDU1NTk2LDE5MzI3NzU2ODgsLTI4NjM4MTQz
Miw0MjM4NTI3OCwxMzg5MTA3MjUyLDE3NTk3ODk4NzgsLTEyOD
g0NzUyNTMsODg3NTI2MTg4LC00NzczNzQxNjAsLTQxNDU5NTUw
OCwxODM1OTg5Nzk5LC0xODMzNTY3NTUzLC0yMDg1NjM4Mjk4LC
0xMjk1MDI4Mjk3LDExNjMxMTc2MDUsMTk3OTA5NDAwMCwxODA4
NzIxNDI0XX0=
-->