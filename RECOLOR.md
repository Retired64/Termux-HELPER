## GUIA RECOLOR SKINS SM64EX-COOP
* PRIMERO OBTENER TUS ARCHIVOS 
1. model.inc
2. geo.inc.c
3. geo_header.h
* Estos 3 Archivos conforman a un modelo `mario_geo.bin` para el juego.
esos 3 archivos al agregarlos a `Dynos/packs/` dentro de una carpeta llamada `mario` El juego Automaticamente convierte esos 3 archivos en un 
`mario_geo.bin` ...
___________________________________________________________________________

Llamaremos a esta diagonal `/` Carpetas cada divisor es una carpeta entonces 
el modelo debe ir en ....
tu almacenamiento interno en la carpeta 
`com.owokitty.sm64excoop/Dynos/packs/Tucarpeta/mario/`
dentro de la carpeta `mario` van los 3 archivos sin el modelo `mario_geo.bin`

### una vez identificado eso seguiremos con el recolor

* editaremos una linea en el archivo `geo.inc.c` donde pondremos esta linea adicional justo como en la imagen a continuacion
```
GEO_ASM(0, geo_mario_set_player_colors),
```
![image](https://cdn.discordapp.com/attachments/1120450661050499083/1167352683548643388/Screenshot_20231026-233724_QuickEdit2.png?ex=654dd0e8&is=653b5be8&hm=935d0ce676053c718f8a968841d26e60f1d713f72acae36f09716497122a4ed8&)
agregaras abajo de 
```
GEO_OPEN_NODE(),
LA NUEVA LINEA
```
quedara arriba de todos los
`GEO_ASM(0`
de esa seccion
_______________________________________________________________________________________________________

### model.inc (PARTES, DEL CUERPO)

* Existen distintas partes de color para agregar y se definen como:
`SKIN, GLOVES, HAIR, PANTS, SHOES,`
________________________________________________________________________________________________________
* modificaremos la parte donde se encuentra este codigo
Reemplazando esto:
`gsSPSetLights1`

Por esto:
`gsSPCopyLightsPlayerPart`(LA_PARTE),
### Ejemolo a continuacion:
![image](https://cdn.discordapp.com/attachments/1120450661050499083/1167354349673005066/Screenshot_20231026-234743_QuickEdit2.png?ex=654dd275&is=653b5d75&hm=361a8d658a80c73c2c33852174702014b03b9a1b2ae1e5010b805515065c47cb&)
### Ejemplo No.2
![image](https://cdn.discordapp.com/attachments/1120450661050499083/1167354367519760465/Screenshot_20231026-234750_QuickEdit2.png?ex=654dd279&is=653b5d79&hm=7e100dc419aaa8dc97b22444eda843923ca9b3e1def52d1c2a273318e57cef8b&)
Se reemplaza la linea completa del codigo `gsSPSetLights1`
por la nueva que seria `gsSPCopyLightsPlayerPart(PARTE_DEL_CUERPO),`

## DESPUES DE FINALIZAR GUARDAR EL ARCHIVO 
* Mover el archivo a /dynos/packs/Tu-Carpeta/mario/
donde en `mario` dentro de esa carpeta van tus 3 archivos obligatorios del modelo

### Guia realizada por Retired64, Basica pero util... !! 

