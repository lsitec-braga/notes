
# Templates for dota messages

## Get Config

Dota envia:

```bash
00:{dotA:X:F}
```

Server envia:

## Set Config

Passo 1 - Enviar `nome do host`

```bash
00:{dotA:D:H:dota-broker.lsitec.org.br}
```

Passo 2 - Enviar `usuario`

```bash
00:{dotA:D:O:}
```

Passo 3 - Enviar `senha`

```bash
00:{dotA:D:A:}
```

Passo 4 - Enviar `host port`

```bash
00:{dotA:D:R:075B}
```

Passo 5 - Enviar `SSL ON`

```bash
00:{dotA:D:D:1}
```

Passo 6 - Enviar `certificado`

```bash
00:{dotA:D:C:XX:XXXXX-----(64)}
```

Passo 7 - Enviar `tipo de certificado`
> 0:CA, 1:Cert, 2:Private

```bash
00:{dotA:D:W:0}
```

Passo 8 - Enviar comando de `Save to EEPROM`

```mqtt
00:{dotA:D:U} 
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc5MzM2MDE3OCw0NTc2NDY1NDNdfQ==
-->