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

---

Como **boa prática**, os componentes são criados dentro de um arquivo de layout, geralmente localizado no caminho: `app/src/main/res/layout/nomeDoArquivo.xml`

Aqui está um exemplo de como ficaria o código dentro desse arquivo

```java
<?xml version="1.0" encoding="utf-8"?>  
<androidx.constraintlayout.widget.ConstraintLayout  
  xmlns:android="http://schemas.android.com/apk/res/android"  
  xmlns:tools="http://schemas.android.com/tools"  
  android:layout_width="match_parent"  
  android:layout_height="match_parent">  
  
 <TextView  android:id="@+id/textView"  
  android:layout_width="wrap_content"  
  android:layout_height="wrap_content"  
  android:text="Diego Braga"  
  tools:layout_editor_absoluteX="7dp"  
  tools:layout_editor_absoluteY="120dp" />  
</androidx.constraintlayout.widget.ConstraintLayout>
```

### Toast

Mensagem de texto que aparece por um período na parte inferior da tela, geralmente refere-se a alguma ação que foi executada para o usuário

```java
import android.widget.Toast;

// Toast.makeText(context, message, time).show()
Toast.makeText(this, "Mensagem desejada", Toast.LENGTH_LONG).show();
```

### ListView

FrontEnd

```xml
<ListView  
  android:id="@+id/activity_main_students_list"  
  android:layout_width="match_parent"  
  android:layout_height="match_parent" />
```

BackEnd

```java
import android.widget.ArrayAdapter;  
import android.widget.ListView;

// Define a lista
List<String> students = new ArrayList<>(Arrays.asList("Diego", "Carlos", "Bruno"));  
ListView studentsList = findViewById(R.id.activity_main_students_list);  
studentsList.setAdapter(new ArrayAdapter<>(this, android.R.layout.simple_list_item_1, students));
```

### FloatingActionButton

FrontEnd

```xml
<com.google.android.material.floatingactionbutton.FloatingActionButton  
  android:id="@+id/activity_main_add_student"  
  android:layout_width="match_parent"  
  android:layout_height="wrap_content"  
  app:fabSize="normal"  
  android:layout_alignParentEnd="true"  
  android:layout_alignParentBottom="true"  
  android:layout_marginEnd="24dp"  
  android:layout_marginBottom="24dp"  
  android:clickable="true" />
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ2NzAyODQ1MiwxNzA5MTcxNDUsLTU1OT
Q4MzU2MSw0MDY2NjcyODksNTQ3MjIxMzgyLDg2NDQwMjQ4MCw3
OTA1Mzg3NDgsNzMwOTk4MTE2XX0=
-->