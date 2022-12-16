# Config Server

## MQTT

### Broker MQTT

- [EMQX](https://www.emqx.com/en)

### Client MQTT

- [Paho](https://www.eclipse.org/paho/)

## Flow da conexão

### Requisitos

> SERIAL_NUMBER_DOTA é personalizado de acordo com o número de série do dota em questão

1. dotA **publica** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA`
2. dotA está **inscrito** no tópico `CFG_SUB/SERIAL_NUMBER_DOTA`
3. listener-dota está **inscrito** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA`
4. listener-dota **publica** no tópico `CFG_SUB/SERIAL_NUMBER_DOTA`

### 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM1NzU0OTM1MSwtNTcxMTgwNDQzXX0=
-->