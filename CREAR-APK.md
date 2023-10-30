Crear una aplicación APK simple que muestre la hora en Android puede ser un proyecto interesante. Aquí tienes una guía paso a paso para crear una aplicación básica que haga esto utilizando Termux y Python.

**Paso 1: Instala Termux y Actualiza el Sistema**

Asegúrate de tener la aplicación Termux instalada en tu dispositivo Android. Abre Termux y actualiza el sistema con:

```shell
pkg update
```

**Paso 2: Instala Python en Termux**

Si no tienes Python instalado en Termux, instálalo con el siguiente comando:

```shell
pkg install python
```

**Paso 3: Crea un Script en Python para Mostrar la Hora**

Crea un script Python para mostrar la hora. Puedes usar un editor de texto dentro de Termux, como Nano, para crear un archivo Python. Por ejemplo:

```shell
nano hora.py
```

Dentro de `hora.py`, escribe el siguiente código Python para mostrar la hora:

```python
import time

hora_actual = time.strftime("%H:%M:%S")
print("Hora actual:", hora_actual)
```

Guarda el archivo (en Nano, presiona `Ctrl` + `O`, luego `Enter`, y para salir, presiona `Ctrl` + `X`).

**Paso 4: Ejecuta el Script Python**

Ejecuta el script Python para asegurarte de que muestra la hora correctamente:

```shell
python hora.py
```

**Paso 5: Crea un Archivo de Manifiesto de la Aplicación (AndroidManifest.xml)**

Ahora necesitas crear un archivo de manifiesto para tu aplicación, que describirá la información básica de la aplicación, como el nombre, el ícono y la actividad principal.

Crea un archivo llamado `AndroidManifest.xml` con un editor de texto:

```shell
nano AndroidManifest.xml
```

Dentro de `AndroidManifest.xml`, copia y pega el siguiente contenido:

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.tu_nombre_de_paquete"
    android:versionCode="1"
    android:versionName="1.0" >

    <uses-sdk
        android:minSdkVersion="16"
        android:targetSdkVersion="28" />

    <application
        android:label="@string/app_name"
        android:icon="@mipmap/ic_launcher" >

        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>
</manifest>
```

Reemplaza `"com.tu_nombre_de_paquete"` con el nombre de tu paquete de la aplicación.

**Paso 6: Crea un Archivo de Actividad (MainActivity.java)**

Crea un archivo de actividad que se encargará de mostrar la hora. Puedes utilizar un editor de texto para crear un archivo Java. Por ejemplo:

```shell
nano MainActivity.java
```

Dentro de `MainActivity.java`, copia y pega el siguiente código Java:

```java
package com.tu_nombre_de_paquete;

import android.app.Activity;
import android.os.Bundle;
import android.widget.TextView;
import java.text.SimpleDateFormat;
import java.util.Date;

public class MainActivity extends Activity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        TextView textView = findViewById(R.id.textView);

        SimpleDateFormat sdf = new SimpleDateFormat("HH:mm:ss");
        String hora = sdf.format(new Date());

        textView.setText("Hora actual: " + hora);
    }
}
```

**Paso 7: Crea un Diseño de Interfaz de Usuario (activity_main.xml)**

Crea un archivo XML que defina el diseño de la interfaz de usuario. Puedes utilizar un editor de texto para crear un archivo XML. Por ejemplo:

```shell
nano res/layout/activity_main.xml
```

Dentro de `activity_main.xml`, copia y pega el siguiente código XML:

```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingLeft="16dp"
    android:paddingTop="16dp"
    android:paddingRight="16dp"
    android:paddingBottom="16dp"
    tools:context=".MainActivity" >

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hora actual: 00:00:00"
        android:textSize="24sp" />
</RelativeLayout>
```

Este archivo define un diseño simple con un `TextView` para mostrar la hora.

**Paso 8: Crea un Icono de Aplicación**

Crea un ícono para tu aplicación y guárdalo en la carpeta `res/mipmap` con el nombre `ic_launcher.png`.

**Paso 9: Compila la Aplicación**

Para compilar la aplicación, usa el siguiente comando:

```shell
aapt package -f -M AndroidManifest.xml -I /data/data/com.termux/files/usr/share/apktool/framework/1.apk -S res -F bin/app.apk
```

**Paso 10: Instala la Aplicación**

Instala la aplicación que has creado con:

```shell
pm install -r bin/app.apk
```

**Paso 11: Ejecuta la Aplicación**

Ahora puedes ejecutar la aplicación desde el lanzador de aplicaciones de Android.

Este es un proceso simplificado para crear una aplicación APK básica en Termux que muestra la hora. Ten en cuenta que este es un proyecto bastante rudimentario, pero te proporciona una idea de cómo se crea una aplicación simple en Android. Para aplicaciones más complejas, se recomienda utilizar un entorno de desarrollo como Android Studio.
