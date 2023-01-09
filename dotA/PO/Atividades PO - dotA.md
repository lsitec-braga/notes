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
- [Monitor AWS](https://sa-east-1.console.aws.amazon.com/cloudwatch/home?region=sa-east-1#dashboards:name=Monitora_Server)
- [Main Database](http://dota-mysql.mobile.lsitec.intranet/phpmyadmin/index.php)
- [Backup Database](https://dotabkp-mysql.mobile.lsitec.intranet/phpmyadmin/index.php)
- [Server de configuração](http://10.0.160.47:18083/#/login?to=/dashboard/overview)

## Assumindo projeto

Ao assumir o projeto, os seguintes pontos devem ser dominados:

- [ ] Entender o que se espera do produto para as próximas semanas, meses (visão do cliente/stakeholder)
- [ ] Analisar Product Backlog
- [ ] Analisar os custos do AWS
- [ ] Analisar a plataforma do dota 1 (pegar acesso de admin com o Alexandre)
- [ ] Analisar a plataforma do dota 2
- [ ] Entender Infra do dota 1 (vou te passar um resumo e o acesso)
- [ ] Entender Infra do dota 2 (pedir acesso admin para o Alexandre)

## Tarefas diárias

- Enviar um resumo no skype (no final do expediente) sobre o progresso da correção de bugs com o seguinte template:

```
Report 06/01/2023
-----------------
Total de issues abertas: X
Issues abertas: 19, sendo 6 novas adicionadas hoje
2 issues reabertas
10 issues em validação
X issues corrigidas
```

```
Report 06/01/2023
-----------------
Total de issues relacionadas a bugfix: 43
Issues fechadas: 24
Issues ainda abertas: 19, sendo 6 novas adicionadas e 2 reabertas hoje
10 issues em validação
9 issues em desenvolvimento
```

- Enviar um resumo das atividades restantes para o Ickson

```
segue a lista resumida das atividades pendentes:
- Corrigir Bugs: #38, #43, #57, #58, #59
- Fazer itens de qualidade de vida: #61, #62, #63
- Auxiliar na avaliação pós teste de estresse sobre a infra. 
```

- Após a daily, atualizar planilha do projeto de acordo com o que foi falado na daily e conferir o progresso das tasks
- Acompanhar o Welington nos testes e garantir que os bugfix foram executados (garantir a qualidade do produto)

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

## Acordo com o Ickson



Ickson, seguem as atividades para conclusão:
1. Resolver issues que foram/estão sendo reportadas no github (As novas issues criadas são referentes à bugs encontrados no sistema, performance e funcionalidades que não estão tendo o comportamento esperado de acordo com o documento de requisitos)
2. Ajustes simples para melhorar a qualidade de vida do sistema
	2.1. Botão de filtrar por período disponível sem a necessidade de expandir o ponto no painel de controle
	2.2. Tooltip ao deixar o mouse em cima dos botões presentes nos cards dos pontos no painel de controle
	2.3. Manter o mesmo padrão de cores da legenda dos gráficos
	2.4. O ponto que estiver sem conexão nos últimos dias, ao ser expandido, deve apresentar gráficos de seus sensores, mesmo que vazio. Além disso, deve ser possível a filtragem de dados por período, para resgatar dados enquanto havia conexão
3. Garantir que funcionalidades que funcionavam na plataforma Dota 1 estão funcionando na Dota 2
4. Auxiliar na avaliação pós teste de estresse sobre a infra.

Funcionalidades referentes no item 3:
- Conexão com os dotAs
- Painel de controle
- Gerenciamento e conexão com os pontos
- Filtragem de pontos
- Gerenciamento de empresas
- Ativação e tratamento de alarmes
- Geração dos gráficos dentro do painel de controle
- Filtragem dos dados dentro dos gráficos que serão gerados
- Visualização dos gráficos de todos os sensores (temperatura, porta, tensão, pânico)
- Download dos dados gerados nos gráficos
- Perfis de usuários
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzU2NjM3NjMxLC02NjU5NTU4NDAsLTM3MD
Q4MjI4OCw1ODMxMTczNSwyNDIwMDkzODAsOTU5NzAyODAxLDQ2
NDU3Mzk1OSw2NzkzMzk3MTYsLTEwMDYwNTcwMzcsLTE3NzE2NT
MzODQsLTI3NDIwNzI3MywtMTI5ODI5MzA2NiwtMTgzMDUxMjI1
MCwtNDg0MjAzOTQ5XX0=
-->