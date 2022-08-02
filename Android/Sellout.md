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

Faça o build do APK pelo Android Studio e suba o apk para o device

```bash
adb push C:\Users\diego.braga\Documents\Multilaser\sellout\sellout-training\app\build\outputs\apk\debug\app-debug.apk system/priv-app/Sellout
```

## Adicionar permissões privilegiadas ao app

Caso o apk possuir permissões privilegiadas o sistema ficará travado na tela de boot. Isso acontece porque tais permissões precisam estar definidas.

Seguem os passos para resolver esse problema:

Coletar o arquivo

```bash
adb pull system/etc/permissions/privapp-permissions-platform.xml
```
    
Alterar o arquivo, adicionando as seguintes tags/permissões relacionadas ao apk

```xml
<privapp-permissions package="br.org.lsitec.training.sellout">
	<permission name="android.permission.READ_EXTERNAL_STORAGE"/>
	<permission name="android.permission.WRITE_EXTERNAL_STORAGE"/>
	<permission name="android.permission.DELETE_PACKAGES"/>
	<permission name="android.permission.INSTALL_PACKAGES"/>
	<permission name="android.permission.READ_PRIVILEGED_PHONE_STATE"/>
	<permission name="android.permission.WRITE_SETTINGS"/>
	<permission name="android.permission.INTERACT_ACROSS_USERS"/>
	<permission name="android.permission.INTERACT_ACROSS_USERS_FULL"/>
</privapp-permissions>
```

Faça root e remonte o AVD

```
adb root
adb remount
```
    
Devolver arquivo editado

```bash
adb push privapp-permissions-platform.xml /system/etc/permissions/
```

Reinicie o dispositivo
    
```bash
adb reboot
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTUzNTM5MDMzOF19
-->