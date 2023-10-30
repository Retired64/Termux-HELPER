El comando `lua-fmt -i mi_script.lua` se utiliza para formatear un archivo Lua (`mi_script.lua`) aplicando un estilo de codificación consistente. `lua-fmt` es una herramienta que ajusta la estructura y el formato del código Lua de acuerdo con las convenciones de estilo. Aquí tienes un ejemplo de cómo funciona este comando:

Supongamos que tienes un archivo Lua llamado "mi_script.lua" con el siguiente código desordenado:

```lua
-- mi_script.lua

function saludar(nombre)
    print("Hola, " ..nombre .. "!")
end

for i=1,3 do
if i == 2 then print("Dos") else
print("Uno")
end
end

```

El código en este archivo no sigue una estructura clara y no está bien formateado según las convenciones de estilo. Ahora, al ejecutar el comando `lua-fmt -i mi_script.lua`, el código se reformateará y se ajustará al estilo de codificación comúnmente aceptado en Lua. Después de ejecutar el comando, el contenido del archivo "mi_script.lua" se verá más organizado y legible:

```lua
-- mi_script.lua

function saludar(nombre)
    print("Hola, " .. nombre .. "!")
end

for i = 1, 3 do
    if i == 2 then
        print("Dos")
    else
        print("Uno")
    end
end
```

El comando `lua-fmt` ha realizado varias modificaciones:

1. Añadió espacios alrededor del operador de concatenación (`..`) para mejorar la legibilidad.
2. Añadió espacios alrededor de operadores de comparación (`==`) y de asignación (`=`).
3. Añadió sangría para identar el código de manera consistente.
4. Agregó líneas en blanco para separar bloques lógicos de código.
5. Formateó las sentencias `if` y `else` para que sigan una estructura más legible y convencional.

En resumen, el comando `lua-fmt` ajusta automáticamente el formato del código Lua para que siga las convenciones de estilo, lo que mejora la legibilidad y la consistencia del código. Esto facilita la colaboración y el mantenimiento del código a lo largo del tiempo.
