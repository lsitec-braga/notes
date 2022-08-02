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

## Remount para SDK menor ou igual a 28

Fazer root

```bash
adb root
```

Fazer remount

```bash
adb remount
```

## Remount para SDK maior ou igual a 29

Fazer root no dispositivo

```bash
adb root
```

Desativar secure boot do adb

```bash
adb shell avbctl disable-verification
```

Reiniciar dispositivo

```bash
adb reboot
```

Fazer root e remontar dispositivo

```bash
adb root
adb remount
```

## Embarque do apk na system

Seguir os passos de Remount para que seja possível manipular a pasta system do device e embarcar um apk com permissão de sistema.

Acessar o terminal do Android e criar a pasta do app

```bash
adb shell
mkdir system/priv-app/<pasta_do_app>
``` 

Voltar ao terminal do Windows

```bash
exit
```

Subir o apk

```bash
adb push <nome_do_app.apk> system/priv-app/<pasta_do_app>
```


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0ODk5MDg2OCwyNTU5MDE5MzNdfQ==
-->