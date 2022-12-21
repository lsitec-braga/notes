# Sellout

## Template da descrição da Issue

```markdown
## Details of the issue:

- WHAT:
- HOW:
- WHY:

## Tasks:

- [ ] Any task you want to add
```

## Acessar diretório do projeto

```bash
cd ~/Documents/Multilaser/Sellout/sellout
```

## Acessar ao root do AVD

Editar a variável do sistema `Path` e adicione os seguintes caminhos:
- `C:\Users\diego.braga\AppData\Local\Android\Sdk\platform-tools\`
- `C:\Users\diego.braga\AppData\Local\Android\Sdk\build-tools\32.0.0\`
- `C:\Users\diego.braga\AppData\Local\Android\Sdk\emulator`

Listar emuladores

```bash
emulator -list-avds
```

Iniciar um device de acordo com a lista apresentada

```bash
emulator -avd Pixel_3_XL_API_30 -writable-system
```

```bash
emulator -avd Pixel_3_XL_API_31 -writable-system
```

```bash
emulator -avd Pixel_5_API_31 -writable-system -no-snapshot-load -no-boot-a
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

Fazer remount do dispositivo

```bash
adb remount
```

Reiniciar dispositivo

```bash
adb reboot
```

## Embarque do apk na system

Seguir os passos de Remount para que seja possível manipular a pasta system do device e embarcar um apk com permissão de sistema.

Fazer root e remontar dispositivo

```bash
adb root
```

```bash
adb remount
```

Acessar o terminal do Android e criar a pasta do app

```bash
adb shell
```

```bash
mkdir system/priv-app/Sellout
``` 

Voltar ao terminal do Windows

```bash
exit
```

Fazer o build do APK pelo Android Studio e suba o apk para o device

```bash
adb push C:\Users\diego.braga\Documents\Multilaser\sellout\sellout\app\build\outputs\apk\debug\app-debug.apk system/priv-app/Sellout
```

## Adicionar permissões privilegiadas ao app

Caso o apk possuir permissões privilegiadas o sistema ficará travado na tela de boot. Isso acontece porque tais permissões precisam estar definidas. Seguem os passos para resolver esse problema:

Pegue o arquivo para editá-lo

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

```bash
adb root
```

```bash
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

## Apagar dados do app Sellout

Já que essa opção é travada por métodos convencionais, é necessário usar os seguintes comandos no terminal

```bash
adb root
```

```bash
adb remount
```

```bash
adb shell pm clear br.org.lsitec.training.sellout
```

Outra alternativa seria o comando abaixo (às vezes não funcionando conforme o esperado)

```bash
adb root
adb remount
adb shell rm -rf data/data/br.org.lsitec.training.sellout
```

## Analisar DB local do app

No terminal do windows

```bash
adb root
```

```bash
adb shell
```

No terminal do Android

```bash
sqlite3 data/data/br.org.lsitec.training.sellout/databases/sellout.db
```

No terminal do sqlite3

```bash
.dump
```

## Recompilar app após mudança no código fonte

Fazer build do novo apk no Android Studio
Fazer root no ADB

```bash
adb root
```

Fazer remount no ADB

```bash
adb remount
```

Limpar dados do projeto do Sellout

```bash
adb shell pm clear br.org.lsitec.training.sellout
```

Adicionar o .apk para o sistema

> Para Windows/Powershell

```powershell
adb push C:\Users\diego.braga\Documents\Multilaser\sellout\sellout\app\build\outputs\apk\debug\app-debug.apk system/priv-app/Sellout
```

> Para Linux/Bash

```bash
adb push ~/Documents/Multilaser/sellout/sellout/app/build/outputs/apk/debug/app-debug.apk system/priv-app/Sellout
```

Fazer build no projeto `ctrl + F5`

Reiniciar o dispositivo

```
adb reboot
```

## Testar app no dispositivo físico

1. Altere no arquivo `AndroidManifest.xml` o trecho do código contendo o main service

```xml
<service  
  android:name=".service.MainService"  
  android:enabled="true"  
  android:exported="true" />
```

2. Rode o aplicativo no Android Studio com o dispositivo físico conectado e habilitado para debug
3. Inicie o app no dispositivo físico através do seguinte comando no terminal do computador

```bash
adb shell am start-foreground-service br.org.lsitec.training.sellout/.service.MainService
```

## Descobrir timer do Work

```bash
adb shell dumpsys jobscheduler | findstr br.org.training.sellout
```
<!--stackedit_data:
eyJwcm9wZXJ0aWVzIjoiZXh0ZW5zaW9uczpcbiAgcHJlc2V0Oi
BnZm1cbiIsImhpc3RvcnkiOlstMjA5MTQxMjc5NywxMzI4MjQ0
MzE4LC00MTI3MzYwNzksOTA5MjI4MjMsLTEzNjA0NzEyODMsNT
g5Mzk2NTA1LDEwODE0ODYxMDcsMTU0NTE3ODYyNiwtMTM2NTAw
MzgwMSwxMTc4ODI4NzM4LC03ODgxOTk3NTddfQ==
-->