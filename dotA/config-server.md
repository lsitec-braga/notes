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
kill -9 3139
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTcyNTk4MjgwLDI2NTcyMDgwOCwyMTI0Mz
U3MjgxLC0xMTc2ODg3NDkwLDE4MDczNTcwNzAsMTMxMjQxMTI4
MywtMjExNTEzODkyMSwxODgxNTM1NDQyLC0yMTQ1NTgyODk1LD
k0NzI1MzM5NiwxNTAxMDgxMDQwLDc4MDAxMjc1OSwtMTY0ODEy
NTg3MiwtNTM4NTc1MDk0LDcyNTc1NDEzMCwtMTU3ODU1NjM0MC
wtNTcxMTgwNDQzXX0=
-->