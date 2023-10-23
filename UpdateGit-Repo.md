
## Crear un repositorio desde cero en GitHub utilizando Termux en tu dispositivo Android es un proceso que implica algunos pasos clave. A continuación, te proporciono una guía paso a paso junto con algunos consejos útiles:

**Paso 1: Instala Git y Termux**

Si aún no tienes Git y Termux instalados en tu dispositivo Android, puedes obtenerlos desde la tienda de aplicaciones de Google Play Store. Git es necesario para gestionar repositorios, y Termux proporciona una interfaz de línea de comandos.

**Paso 2: Configura Git**

Antes de crear un repositorio, configura tu información de Git en Termux. Esto incluye tu nombre de usuario y tu dirección de correo electrónico. Reemplaza "TUNOMBRE" y "TUCORREO@EJEMPLO.COM" con tus propios datos:

```shell
git config --global user.name "TUNOMBRE"
git config --global user.email "TUCORREO@EJEMPLO.COM"
```

**Paso 3: Inicia una Sesión en GitHub**

Asegúrate de tener una cuenta en GitHub. Si no tienes una, puedes crear una en [GitHub.com](https://github.com).

**Paso 4: Crea un Token de Acceso Personal (Opcional)**

Para mejorar la seguridad, puedes crear un token de acceso personal en GitHub. Esto se puede utilizar en lugar de tu contraseña. Puedes generar un token en la configuración de tu cuenta de GitHub en la sección "Tokens de acceso personal".

**Paso 5: Crea un Nuevo Repositorio**

1. Abre Termux y navega al directorio donde deseas crear el repositorio. Por ejemplo, puedes usar `cd ~/storage/shared` para acceder a una carpeta compartida.

2. Luego, crea un nuevo directorio para tu proyecto:

```shell
mkdir NOMBRE-DE-TU-PROYECTO
```

3. Accede al directorio de tu proyecto:

```shell
cd NOMBRE-DE-TU-PROYECTO
```

4. Inicializa un repositorio Git en ese directorio:

```shell
git init
```

5. Crea un archivo README.md (esto es opcional, pero es una buena práctica tener un README en tu repositorio):

```shell
touch README.md
```

6. Agrega y confirma los cambios iniciales:

```shell
git add .
git commit -m "Primer commit"
```

**Paso 6: Conecta el Repositorio a GitHub**

1. Crea un repositorio vacío en GitHub. Puedes hacerlo desde la página principal de GitHub haciendo clic en el botón "New" (Nuevo) en la parte superior derecha.

2. Sigue las instrucciones para crear el repositorio. No inicialices el repositorio con un archivo README, ya que ya tienes uno.

3. Una vez creado, GitHub te proporcionará una URL que se parece a `https://github.com/TU-USUARIO/NOMBRE-DE-TU-REPOSITORIO.git`.

4. Conecta tu repositorio local de Termux a tu repositorio de GitHub utilizando esa URL. Reemplaza `TU-USUARIO` y `NOMBRE-DE-TU-REPOSITORIO` con tus propios datos:

```shell
git remote add origin https://github.com/TU-USUARIO/NOMBRE-DE-TU-REPOSITORIO.git
```

5. Sube tus archivos locales al repositorio de GitHub:

```shell
git push -u origin main
```

Si estás usando una rama diferente en lugar de `main`, asegúrate de cambiar el nombre de la rama en el comando anterior.

**Paso 7: Autenticación (Token de Acceso Personal o Contraseña)**

Cuando ejecutes `git push`, es posible que se te solicite autenticación. Puedes usar tu nombre de usuario y contraseña de GitHub, o si has creado un token de acceso personal, puedes usarlo. Para usar el token, simplemente pégalo en lugar de tu contraseña.

**Paso 8: Confirma tu Repositorio en GitHub**

Visita la página de tu repositorio en GitHub en un navegador web para confirmar que tus archivos se han cargado correctamente.

¡Felicidades! Has creado un repositorio desde cero utilizando Termux en tu dispositivo Android y lo has conectado a GitHub. Ahora puedes comenzar a desarrollar tu proyecto en el repositorio.
## EXTRAS

Para agregar un archivo README.md a tu repositorio ya existente en GitHub desde Termux, puedes seguir estos pasos:

1. **Clona el Repositorio**:
   - Abre Termux en tu dispositivo Android.
   - Clona el repositorio existente en tu dispositivo utilizando el comando `git clone`. Por ejemplo, para clonar el repositorio "OoO", puedes ejecutar:

   ```shell
   git clone https://github.com/Retired64/OoO.git
   ```

   Esto creará una copia local del repositorio en tu dispositivo.

2. **Crea el Archivo README.md**:
   - En Termux, utiliza un editor de texto como nano o vim para crear un archivo README.md. Puedes ejecutar:

   ```shell
   nano OoO/README.md
   ```

   Esto abrirá el editor de texto nano con un archivo nuevo llamado README.md.

3. **Edita el README.md**:
   - Agrega el contenido que desees al archivo README.md utilizando el editor de texto. Puedes incluir información sobre tu proyecto, instrucciones de uso, descripción, etc.

4. **Guarda y Sale del Editor**:
   - En nano, para guardar los cambios, presiona `Ctrl + O`, luego presiona "Enter". Para salir de nano, presiona `Ctrl + X`.

5. **Agrega, Confirma y Sube los Cambios**:
   - Luego de haber creado el archivo README.md y editado su contenido, utiliza los siguientes comandos para agregar, confirmar y subir los cambios al repositorio:

   ```shell
   cd OoO  # Entra al directorio del repositorio
   git add README.md  # Agrega el archivo README.md
   git commit -m "Agregado README.md"  # Confirma los cambios
   git push origin main  # Sube los cambios a GitHub (o reemplaza "main" por la rama correspondiente)
   ```

   Asegúrate de estar en el directorio del repositorio antes de ejecutar estos comandos.

6. **Visita GitHub**:
   - Ahora, visita tu repositorio en GitHub (https://github.com/Retired64/OoO) desde un navegador web para ver el README.md recién agregado.

Tu repositorio debería mostrar ahora el archivo README.md que creaste y editaste desde Termux.
