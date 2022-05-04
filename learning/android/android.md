# Android

## O que é?

- Sistema operacional _open source_ baseado em Linux
- Usado em sua maioria em celulares e tablets, mas também pode ser encontrado em TVs, Notebooks, carros, microcomputadores e _wearables_ (relógios e pulseiras inteligentes)

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

> Esse código adicionado serve para que o arquivo `MainActivity.java` seja identificada pelo Android como o arquivo a ser iniciado

## Componentes

Para adicionar componentes é necessário primeiro sobrescrever estados de ciclos de vida da Activity, nesse caso, o método a ser sobrescrito é chamado de  `onCreate()` 

```java
// MainActivity.java
import androidx.annotation.Nullable;

@Override  
protected void onCreate(@Nullable Bundle savedInstanceState) {  
    super.onCreate(savedInstanceState);
}
```

Em seguida, é adicionado o seguinte método dentro da classe `MainActivity`

```java
// O argumento dentro do método é baseado no nome adicionado no
// arquivo de layout
setContentView(R.layout.activity_main);
```

Como **boa prática**, os componentes são criados dentro de um arquivo de layout, geralmente localizado no caminho: `app/src/main/res/layout/nomeDoArquivo.xml`

### Toast

Mensagem de texto que aparece por um período na parte inferior da tela, geralmente refere-se a alguma ação que foi executada para o usuário

```java
import android.widget.Toast;

// Toast.makeText(context, message, time).show()
Toast.makeText(this, "Mensagem desejada", Toast.LENGTH_LONG).show();
```

### View



<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM2MjIxMDY3MCwtNTU5NDgzNTYxLDQwNj
Y2NzI4OSw1NDcyMjEzODIsODY0NDAyNDgwLDc5MDUzODc0OCw3
MzA5OTgxMTZdfQ==
-->