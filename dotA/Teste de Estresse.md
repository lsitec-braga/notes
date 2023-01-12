# Teste de estresse

## Objetivos

- Encontrar a quantidade limite de dotas simultâneos que o sistema suporta  
- Definir se a infraestrutura atual é o suficiente para suportar o sistema como um todo com vários usuários acessando a plataforma simultaneamente

## Procedimento do teste

1. O teste será iniciado com 10 dotas simultâneos, devendo acordar entre os testes quem ficará com quantidade X de dotas para alcançar o número total  
2. Se o sistema suportar a quantidade testada, vamos aumentar em 50% de sua quantidade para averiguar se segue suportando  
3. Se o sistema não suportar a quantidade testada, vamos reduzir em 50% da quantidade de aumento e ver se o valor reduzido suporta  
4. Seguir os passos 2 e 3, ajustando conforme a necessidade, até chegar próximo do valor limite que define se o sistema vai continuar funcionando ou não

Obs.: Por ser um teste de estresse, é possível que ocorra alteração nos custos da AWS, portanto, devemos tomar cuidado para não gerar muita diferença

## Papéis

- Responsável pelo script de estresse: Ickson  
- Responsáveis por adaptar o script de estresse: Diego, Victor e Henrique (opcional)  
- Responsáveis por estressar o sistema: Alexandre, Diego, Victor e Welington  
- Responsável por monitorar o sistema: Jefferson  
- Opcionais: Henrique e Jake

## Ferramentas para avaliação

- [Planilha](https://docs.google.com/spreadsheets/d/1vYYiKfqUQ9IWmB7hvXE9hFXUomil17JVDZPd0AwVaeI/edit#gid=840597766)
- [CloudWatch](https://sa-east-1.console.aws.amazon.com/cloudwatch/home?region=sa-east-1#dashboards:name=Monitora_Server_EC2)

## Resultados


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgxNTE1MDQzM119
-->