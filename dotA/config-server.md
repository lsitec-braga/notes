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

1. dotA faz **publish** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA` com o seguinte *payload* `03:20220705141322:1:2:0:-11.34:2:22.09:2:1:0:220.14:3:2:0:1:2:0:4:1:0:1`
2. listener-dota está **subscribed** no tópico `CFG_PUB/SERIAL_NUMBER_DOTA` portanto recebe qualquer comando novo que aparecer no tópico
3. listener-dota ao perceber que foi adicionada uma informação no tópico `CFG_PUB/SERIAL_NUMBER_DOTA`, irá enviar  para o tópico `CFG_SUB/SERIAL_NUMBER_DOTA` o seguinte *payload* `RCVOK:03`

> [Documento](https://docs.google.com/document/d/1LJil1iZYlHuiEr4n8OyWY4aa7Qc4jffb/edit) explicando do formato do *payload*

## Acessar servidor com script 

Deixar script rodando mesmo ao fechar o PuTTY

```bash
cd scripts ; nohup python3 broker-listener.py &
```

Finalizar com o processo

```bash
kill -9 1105495
```

Observar serviços relacionados ao broker-listener

```bash
while true; do ps fuxa |grep broker-listener.py|grep -v grep ; sleep 10; echo ------------------; done
```

## Acessar servidor com script 

Deixar script rodando mesmo ao fechar o PuTTY

```bash
sudo nohup npm run log &
```

Finalizar com o processo

```bash
kill -9 3738
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNTM3Mjg1MSwtMTA3Njg0MDc5MiwtMT
c4MzcxODI2NCwtOTEyODQ2NzIyLC0zMzIyNjU2OTQsODM2ODk4
NzgxLDk3MjU5ODI4MCwyNjU3MjA4MDgsMjEyNDM1NzI4MSwtMT
E3Njg4NzQ5MCwxODA3MzU3MDcwLDEzMTI0MTEyODMsLTIxMTUx
Mzg5MjEsMTg4MTUzNTQ0MiwtMjE0NTU4Mjg5NSw5NDcyNTMzOT
YsMTUwMTA4MTA0MCw3ODAwMTI3NTksLTE2NDgxMjU4NzIsLTUz
ODU3NTA5NF19
-->