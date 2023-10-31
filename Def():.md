En Python, `def` se utiliza para definir una función. Una función es un bloque de código reutilizable que realiza una tarea específica. A continuación, te proporciono tres ejemplos de definiciones de funciones en Python, junto con una explicación detallada de cada parte del código:

**Ejemplo 1: Función simple sin argumentos ni valor de retorno**

```python
def saludar():
    print("Hola, mundo!")

# Llamamos a la función para ejecutarla
saludar()
```

- `def saludar():`: Aquí estamos definiendo una función llamada `saludar` sin argumentos. La declaración comienza con la palabra clave `def`, seguida del nombre de la función y paréntesis vacíos (sin argumentos). El colon `:` indica el inicio del bloque de código de la función.
- `print("Hola, mundo!")`: Este es el cuerpo de la función. La función imprime "Hola, mundo!" en la consola.

**Ejemplo 2: Función con argumentos y valor de retorno**

```python
def suma(a, b):
    resultado = a + b
    return resultado

# Llamamos a la función y almacenamos el resultado en una variable
resultado_suma = suma(5, 3)
print("La suma es:", resultado_suma)
```

- `def suma(a, b):`: Estamos definiendo una función llamada `suma` que toma dos argumentos, `a` y `b`.
- `resultado = a + b`: Dentro de la función, calculamos la suma de `a` y `b` y la almacenamos en una variable llamada `resultado`.
- `return resultado`: Devolvemos el valor calculado como resultado de la función.
- Al llamar a la función `suma(5, 3)`, el resultado de la suma se almacena en `resultado_suma` y se imprime.

**Ejemplo 3: Función con argumentos predeterminados**

```python
def saludar(nombre="usuario"):
    print(f"Hola, {nombre}!")

# Llamamos a la función con y sin argumentos
saludar()          # Imprime "Hola, usuario!"
saludar("Juan")    # Imprime "Hola, Juan!"
```

- `def saludar(nombre="usuario"):`: Estamos definiendo una función llamada `saludar` con un argumento `nombre` que tiene un valor predeterminado de "usuario". Esto significa que si no se proporciona un valor al llamar a la función, se utilizará "usuario" como valor predeterminado.
- `print(f"Hola, {nombre}!")`: La función imprime un saludo que incluye el nombre proporcionado o el valor predeterminado si no se proporciona un nombre.

Espero que estos ejemplos te ayuden a comprender cómo se definen y utilizan las funciones en Python.

```python
def saludar(nombre):
    print(f"Hola, {nombre}!")

# Solicitamos el nombre al usuario y luego llamamos a la función
nombre = input("Como te llamas? ")
saludar(nombre)
```

En este código:

1. Definimos la función `saludar` que toma un argumento `nombre`.
2. Luego, fuera de la función, solicitamos al usuario que ingrese su nombre utilizando `input` y almacenamos la entrada en la variable `nombre`.
3. Finalmente, llamamos a la función `saludar` pasando `nombre` como argumento para que la función imprima el saludo con el nombre proporcionado por el usuario.
## mas
Claro, aquí tienes más ejemplos de cómo usar `def` para definir funciones en Python:

**Ejemplo 4: Función con argumentos y sin valor de retorno**

```python
def suma(a, b):
    resultado = a + b

# Llamamos a la función
suma(5, 3)
```

- En este caso, definimos una función `suma` que toma dos argumentos, `a` y `b`. La función calcula la suma de estos números, pero no devuelve ningún valor (no hay `return`).
- Llamamos a la función con `suma(5, 3)`, y la suma se calcula dentro de la función, pero no se almacena ni se muestra en la consola.

**Ejemplo 5: Función con valor de retorno múltiple**

```python
def divide(a, b):
    cociente = a // b  # División entera
    residuo = a % b
    return cociente, residuo

# Llamamos a la función y almacenamos los valores de retorno en variables
resultado_cociente, resultado_residuo = divide(10, 3)
print("Cociente:", resultado_cociente)
print("Residuo:", resultado_residuo)
```

- En este ejemplo, definimos una función `divide` que toma dos argumentos, `a` y `b`. La función calcula tanto el cociente como el residuo de la división de `a` por `b` y los devuelve como una tupla.
- Llamamos a la función con `divide(10, 3)` y almacenamos los valores de retorno en las variables `resultado_cociente` y `resultado_residuo`, que luego imprimimos.

**Ejemplo 6: Función con recursión**

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

# Llamamos a la función para calcular el factorial de 5
resultado = factorial(5)
print("Factorial de 5:", resultado)
```

- En este ejemplo, definimos una función `factorial` que calcula el factorial de un número `n` utilizando recursión.
- La función verifica si `n` es igual a 0 y, si es así, devuelve 1 (caso base). Si no, calcula el factorial multiplicando `n` por el factorial de `n - 1`.
- Llamamos a la función con `factorial(5)` para calcular el factorial de 5 y lo almacenamos en `resultado`.

Estos ejemplos muestran diferentes formas de utilizar `def` para definir funciones en Python, desde funciones simples sin valor de retorno hasta funciones con argumentos y valor de retorno, e incluso funciones recursivas.
### Nivel Medio
aquí tienes ejemplos de funciones interactivas de nivel medio que interactúan con el usuario:

**Ejemplo 7: Calculadora simple**

```python
def calculadora():
    print("Selecciona una operación:")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    
    opcion = input("Ingresa el número de la operación deseada: ")

    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))

    if opcion == "1":
        resultado = num1 + num2
    elif opcion == "2":
        resultado = num1 - num2
    elif opcion == "3":
        resultado = num1 * num2
    elif opcion == "4":
        if num2 != 0:
            resultado = num1 / num2
        else:
            resultado = "Error: División por cero"
    else:
        resultado = "Opción no válida"

    print("Resultado:", resultado)

# Llamamos a la función para realizar cálculos
calculadora()
```

- En este ejemplo, la función `calculadora` interactúa con el usuario para realizar operaciones matemáticas básicas. La función solicita al usuario que seleccione una operación (suma, resta, multiplicación o división), ingrese dos números y luego realiza la operación deseada.

**Ejemplo 8: Conversor de temperatura**

```python
def conversor_temperatura():
    print("Selecciona una opción:")
    print("1. Convertir de Celsius a Fahrenheit")
    print("2. Convertir de Fahrenheit a Celsius")
    
    opcion = input("Ingresa el número de la opción: ")
    temperatura = float(input("Ingresa la temperatura: "))

    if opcion == "1":
        resultado = (temperatura * 9/5) + 32
    elif opcion == "2":
        resultado = (temperatura - 32) * 5/9
    else:
        resultado = "Opción no válida"

    print("Resultado:", resultado)

# Llamamos a la función para realizar conversiones de temperatura
conversor_temperatura()
```

- En este caso, la función `conversor_temperatura` permite al usuario convertir temperaturas entre Celsius y Fahrenheit.

**Ejemplo 9: Juego adivina el número**

```python
import random

def juego_adivina_numero():
    numero_secreto = random.randint(1, 100)
    intentos = 0

    print("Bienvenido al juego Adivina el número.")
    print("Estoy pensando en un número entre 1 y 100. ¡Adivina!")

    while True:
        intento = int(input("Ingresa tu suposición: "))
        intentos += 1

        if intento < numero_secreto:
            print("Demasiado bajo. Intenta de nuevo.")
        elif intento > numero_secreto:
            print("Demasiado alto. Intenta de nuevo.")
        else:
            print(f"Felicitaciones. ¡Adivinaste el número en {intentos} intentos!")
            break

# Llamamos a la función para jugar al juego Adivina el número
juego_adivina_numero()
```

- Este ejemplo implementa un juego interactivo en el que el usuario intenta adivinar un número secreto generado al azar por la computadora.

Estas funciones interactivas permiten a los usuarios realizar cálculos, conversiones o participar en juegos mientras interactúan con el programa.