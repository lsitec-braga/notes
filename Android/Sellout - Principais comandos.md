# Sellout - Principais comandos

## Acesso ao root do AVD

Adicione o emulador ao path do windows com o caminho:
`C:\Users\<seuUser>\AppData\Local\Android\Sdk\emulator`

Liste emuladores

```bash
emulator -list-avds
```

Inicie um device de acordo com a lista apresentada

```bash
emulator -avd <device_name> -writable-system
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjU1OTAxOTMzXX0=
-->