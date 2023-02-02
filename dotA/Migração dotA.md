# Migração dotA

## Plano A - Sucesso na migração

Separar 6 horas do dia 08-Fev-2023 para realizar a migração dos seguintes itens para a instância de Produção:

1. Migrar dados MySQL (Dados das empresas, filiais e usuários)
2. Migrar dados InfluxDB (Dados dos pontos e seus respectivos sensores)
3. Migrar dotAs (Com auxílio do servidor de configuração)

Para não ter imprevistos, fazer a transferência dos dados, tanto MySQL quanto InfluxDB, no dia 06-Fev-2023, para acertar que o procedimento está funcionando conforme o esperado

## Plano B - Problema na migração

### Dúvidas

1. Os comandos de comunicação com o sistema dotA2 são iguais ao dotA1?
2. Ao retornar o dotA para o sistema anterior, precisa voltar a versão do Firmware?
3. É possível voltar uma versão do Firmware compatível com o dotA1?
4. Manter um URL de acesso diferente do atual

### Atividades

1. Adicionar credenciais e certificados de backup que retornem para o dotA1
2. Manter o site antigo (url) para backup e retornarmos o dotA para lá
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA1NTg3MDYwNF19
-->