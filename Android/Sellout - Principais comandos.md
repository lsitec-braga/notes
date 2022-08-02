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

## Remount para SDK <= 28

```bash
adb root
```

```bash
adb remount
```

## Remount para SDK >=29

Root

```bash
adb root
```

```bash
adb shell avbctl disable-verification
```

```bash
adb reboot
```

```bash
adb root
```

```bash
adb remount
```

## Embarque do apk na system
<!--stackedit_data:
eyJoaXN0b3J5IjpbNjY3MDMxMDIzLDI1NTkwMTkzM119
-->