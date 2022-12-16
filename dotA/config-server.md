# Config Server

## IoT

### Broker MQTT

- [EMQX](https://www.emqx.com/en)

### Client MQTT

- [Paho](https://www.eclipse.org/paho/)

## Flow da conexão

### Requisitos

1. dotA **publica** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA`
2. dotA está **inscrito** no tópico `CFG_SUB/SERIAL_NUMBER_DOTA`
3. script está **inscrito** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA`
4. script **publica** no tópico `CFG_SUB/SERIAL_NUMBER_DOTA`

### 

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk0ODgxNzI4MCwtNTcxMTgwNDQzXX0=
-->