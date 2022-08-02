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

## Remount para SDK i 28

Fazer root

```bash
adb root
```

Fazer remount

```bash
adb remount
```

## Remount para SDK >=29

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

Seguir os passos do [Remount](#acesso-ao-root-do-avd)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk0NzM4OSwyNTU5MDE5MzNdfQ==
-->