# Sellout

## Acesso ao root do AVD

Adicione o emulador ao path do windows com o caminho:
`C:\Users\diego.braga\AppData\Local\Android\Sdk\emulator`

Liste emuladores

```bash
emulator -list-avds
```

Inicie um device de acordo com a lista apresentada

```bash
emulator -avd Pixel_3_XL_API_31 -writable-system
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
mkdir system/priv-app/Sellout
``` 

Voltar ao terminal do Windows

```bash
exit
```

Subir o apk

```bash
adb push C:\Users\diego.braga\Documents\Multilaser\sellout\sellout-training\app\build\outputs\apk\debug\app-debug.apk system/priv-app/Sellout
```


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4NDU4MTI3ODAsODk0MDA0MzEyLDI1NT
kwMTkzM119
-->