# Config Server

## MQTT

### Broker MQTT

- [EMQX](https://www.emqx.com/en)

### Client MQTT

- [Paho](https://www.eclipse.org/paho/)

## Definição das conexões MQTT

### Requisitos

> SERIAL_NUMBER_DOTA é personalizado de acordo com o número de série do dota em questão

1. dotA faz **publish** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA`
2. dotA **subscribe** no tópico `CFG_SUB/SERIAL_NUMBER_DOTA`
3. dotA **subscribe** no tópico `STA/SERIAL_NUMBER_DOTA`
4. listener-dota **subscribe** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA`
5. listener-dota faz **publish** no tópico `CFG_SUB/SERIAL_NUMBER_DOTA`
6. listener-dota faz **publish** no tópico `STA/SERIAL_NUMBER_DOTA`

### Fluxo da conexão

1. dotA faz **publish** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA` com o seguinte *payload* 
2. listener-dota está **subscribed** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA` portanto recebe qualquer comando novo que aparecer no tópico
3. listener-dota ao perceber que foi adicionada uma informação no tópico `CFG_PUB/SERIAL_NUMBER_DOTA`, irá enviar  para o tópico `CFG_SUB/SERIAL_NUMBER_DOTA` o seguinte *payload* `RCVOK:{message_id}`

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3Mjk5NDk3NDAsLTU3MTE4MDQ0M119
-->