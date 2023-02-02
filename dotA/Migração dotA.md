# Migração dotA

## Plano A - Sucesso na migração

Separar 6 horas do dia 08-Fev-2023 para realizar a migração dos seguintes itens para a instância de Produção:

1. Migrar dados MySQL (Dados das empresas, filiais e usuários)
2. Migrar dados InfluxDB (Dados dos pontos e seus respectivos sensores)
3. Migrar dotAs (Com auxílio do servidor de configuração)

Para não ter imprevistos, fazer a transferência dos dados, tanto MySQL quanto InfluxDB, no dia 06-Fev-2023, para acertar que o procedimento está funcionando conforme o esperado

## Plano B - Problema na migração

### Dúvidas

1. Os comandos de comunicação com o sistema dotA2 são iguais ao dotA1? Sim
2. Ao retornar o dotA para o sistema anterior, precisa voltar a versão do Firmware? Sim
3. É possível voltar uma versão do Firmware compatível com o dotA1? Sim
4. É possível manter o sistema antigo no ar enquanto não é feito a migração completa para o novo? 

### Atividades

1.  Manter o site antigo para backup caso não dê certo a migração
2.  Adicionar as credenciais e certificados do site antigo no Server de Configuração para migrar de volta
3.  Fazer o Change Host dos Dotas
4.  Assegurar que os Dotas estão funcionando no site dota1
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzgyNzU5NDAsLTE2NDEyNDIxOF19
-->