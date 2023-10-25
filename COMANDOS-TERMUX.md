## APREMDE A MOVERTE EN TERMUX <===-guia Inicial

### Requisitos
* Descarga Termux dando click en donde dice `DESCARGAR` <== Aqui abajo
[DESCARGAR](https://f-droid.org/repo/com.termux_118.apk)
________________________________________________________________________

### LISTA DE COMANDOS BASICOS DE NAVEGACION

```
cd Tu-Carpeta
```
^<= Este Comando te permite entrar a las carpetas dentro de termux
por ejemplo ` cd Tu-Carpeta` entraras a la carpeta : Reemplaza `Tu-Caroeta` por una que tengas en tu termux

### ¿Como saber a que carpeta entrar ?

```
ls
```
* ^^^ `ls` Te permite ver las carpetas de termux en tu directorio actual.

### salir de carpetas o regresar una atras 

```
cd ~
```
^^^^^^ Regresas al directorio principal de Termux 

```
cd ..
```
* con `cd ..` Regresas un directorio Atras del que te encuentres 

### Eliminar archivos

```
rm
```
con `rm` mas el nombre del archivo por ejemplo `rm Tu_archivo.lua` o cualquier archivo .. se eliminara

```
rm -rf 
```
### Eliminar Carpetas
con `rm -rf` eliminas de forma recursiva una carpeta com sus archivos que tiene dentro
ejemplo ` rm -rf Tu-Carpeta`

### acceder al Almacenamiento interno

```
termux-setup-storage
```
* Fundamental para acceder al Almacenamiento interno `Dar Permitir`desoues de ingresar el comando

### Actualizar Termux
```
apt update
```
```
apt upgrade -y
```
* Fundamental A la hora de instalar herramientas o actualizarlas para obtener las mas recientes actualizaciones
### Instalar Herramientas termux 

```
apt install Tu-herramienta
```
### Tambien 
```
pkg install Tu-herramienta
```
* ejemplo ` apt install git` o Tambien `pkg install git` instalaras la herramienta git

### Aceptar o Denegar acciones y/o Permisos

* Cuando vas instalar una herramienta ejemplo `pkg install python` termux preguntara

` do you want continue [y/n]?...`
* Aceptar Significa poner este comando de aqui abajo
```
y
```

a eso significa que si queremos continuar con la instalacion 
responderemos con [ `y` ] En caso de querer continuar
que significa Yes, en cambio [`n`] significa No, 

### Copiar archivos o Carpetas 

```
cp
```
* cp  te permite copiar archivos a otro lugar deseado por ejemplo `cp Tu_archivo.lua /sdcard/` Esto llevara tu archivo a tu memoria interna donde despues podrás verlo desde tu administrador de archivos 
```
cp -r
```
* cp -r  Te permite copiar carpetas de manera recursiva por ejemplo ` cp -r Tu-Carpeta /sdcard/`Esto llevara tu carpeta a tu Almacenamiento interno Donde despues podrás verla desde tu administrador de archivos

## AVISO
### ES IMPORTANTE LEER AUNQUE ESTE EN INGLES POSIBLES ERRORES QUE COMETAS EN TERMUX YA QUE EL MISMO TERMUX TE DA LAS SOLUCIONES, SI NO SABES INGLES COPIA EL TEXTO Y PEGALO EN GOOGLE TRADUCTOR PARA ENTENDER. RECUERDA QUE TODOS LOS COMANDOS EJECUTADOS EN TERMUX SE ESCRIBEN `EN INGLES` PARA SU CORRECTO FUNCIONAMIENTO LEER LETRITAS BLANCAS DE TERMUX AYUDARA A TU MEJOR DESEMPEÑO




