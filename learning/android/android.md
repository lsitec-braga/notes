# Android

## O que é?

- Sistema operacional _open source_ baseado em Linux
- Usado em sua maioria em celulares e tablets, mas também pode ser encontrado em TVs, Notebooks, carros, microcomputadores e _wearables_ (relógios e pulseiras inteligentes)
- 

## Activities

- É a partir delas que o App é iniciado

Hierarquia de uma aplicação

- App
	- Activity
		- View
		- Logica

## Iniciando a criação de um App Android

Crie um arquivo chamado `MainActivity.java` e adicione o seguinte código:

```java
import android.app.Activity;  
  
public class MainActivity extends Activity {  
  
}
```

Dentro do arquivo `app/src/main/AndroidManifest.xml`, adicione o código abaixo

```java
<application
// código base adicionado
>
// Adicione o código abaixo desse comentário
  <activity android:name=".MainActivity">
    <intent-filter>
	  <action android:name="android.intent.action.MAIN"/>
	  <category android:name="android.intent.category.LAUNCHER"/>
    </intent-filter>
  </activity>
// Adicione o código acima desse comentário
</application>
```

> Esse código adicionado serve para que o arquivo `MainActivitie.java` seja identificada pelo Android como o arquivo a ser iniciado
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM2ODgyNzUzMSw1NDcyMjEzODIsODY0ND
AyNDgwLDc5MDUzODc0OCw3MzA5OTgxMTZdfQ==
-->