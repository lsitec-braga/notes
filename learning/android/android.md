# Android

## O que é?

- Sistema operacional _open source_ baseado em Linux
- Usado em sua maioria em celulares e tablets, mas também pode ser encontrado em TVs, Notebooks, carros, microcomputadores e _wearables_ (relógios e pulseiras inteligentes)
- 

## Activities

- É a partir delas que o App é iniciado
-

Hierarquia de uma aplicação

- App
	- Activity
		- View
		- Logica

## Iniciando a criação de um App Android

Dentro do arquivo `app/src/main/`

```java
<application
// código base adicionado
>
  <activity android:name=".MainActivity">
    <intent-filter>
	  <action android:name="android.intent.action.MAIN"/>
	  <category android:name="android.intent.category.LAUNCHER"/>
    </intent-filter>
  </activity>
</application>
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM4MzEyNTg5OSw4NjQ0MDI0ODAsNzkwNT
M4NzQ4LDczMDk5ODExNl19
-->