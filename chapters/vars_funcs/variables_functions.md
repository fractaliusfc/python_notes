# Funciones *built-in*

Llamaremos funciones *built-in* a todas aquellas funciones que viene por defecto en Python. Esto quiere decir que estarán listas para usarse sin la necesidad de importar algún paquete. En la siguiente tabla podemos ver todas las funciones *built-in*.

| &nbsp;        | &nbsp;          | **Funciones Built-in** | &nbsp;       | &nbsp;         |
|---------------|-----------------|------------------------|--------------|----------------|
| **abs()**     | delattr()       | hash()                 | memoryview() | set()          |
| all()         | dict()          | **help()**             | **min()**    | setattr()      |
| any()         | dir()           | hex()                  | next()       | slice()        |
| ascii()       | divmod()        | id()                   | object()     | sorted()       |
| bin()         | **enumerate()** | **input()**            | oct()        | staticmethod() |
| bool()        | eval()          | int()                  | **open()**   | str()          |
| breakpoint()  | exec()          | isinstance()           | ord()        | sum()          |
| bytearray()   | filter()        | issubclass()           | pow()        | super()        |
| bytes()       | float()         | iter()                 | **print()**  | tuple()        |
| callable()    | format()        | **len()**              | property()   | **type()**     |
| chr()         | frozenset()     | list()                 | range()      | vars()         |
| classmethod() | getattr()       | locals()               | repr()       | **zip()**      |
| compile()     | globals()       | map()                  | reversed()   | \_\_import\_\_()  |
| complex()     | hasattr()       | **max()**              | **round()**  | &nbsp;         |

Se puede encontrar una descripción detallada de estas funciones en [documentación oficial](https://docs.python.org/3.9/library/functions.html).

Probemos algunas funciones:

```python
print('Hola Mundo') # Imprime el mensaje y/variable
len('Hola mundo') # Cuenta el número de caractéres
type('Hola Mundo') # Revisa el tipo de dato
str(10) # convierte el valor entero a string
int('10') # convierte la string a el valor entero
float(10) # convierte el valor entero a decimal
input('Escribe tu nombre') # toma el input del usuario
```

Si se requiere ayuda, se puede usar el comando `help`. Por ejemplo:

```python
help(str) # Da información sobre una string
```

EL nombre de estas funciones son **palabras reservadas**. Por lo que no se pueden usar para declarar variables.

# Variables

En general, una variable guarda datos en la memoria de la computadora. Es decir, una variable hace referencia a una dirección en memoria en donde los datos son guardados. Las variables tienen un nombre o identificador, seguido de un signo `=` y el dato que queremos que guarde. A este proceso se le llama **declaración de variables**. Se recomienda que el nombre de las variables este relacionado con lo que guarda. Por ejemplo

```python
aceleracion = 9.81
acel = 9.81
g = 9.81
```

Existen ciertas reglas para el nombre de variables:

> 1.- El nombre no puede iniciar con un número
>
> 2.- El nombre debe de inicar con una letra o un guión bajo
>
> 3.- El nombre solo puede contener caracteres alfa-numericos y guiones bajos

Se debe de tomar en cuenta python diferencia entre mayúsculas y minúsculas (*case-sensitive*)

Algunos nombres válidos de variables son:

```python
nombre
apellido
edad
pais
ciudad
ciudad_nacimiento
_reservado
```

Algunos nombres no válidos:
```python
ciudad-nacimiento
ciudad@nacimiento
ciudad$nacimiento
num-1
1num
```

Podemos usar la función `print` para mostrar los datos guardados en las variables:

```python
nombre = 'Carlos'
print(nombre)
print('Hola ', nombre)
```

También podemos ver el uso de la función `len`

```python
nombre = 'Carlos'
print(nombre)
len(nombre)
```

## Declaración de varias variables en una sola línea

Podemos declarar varias variables de la siguiente manera:

```python
nombre, apellido, pais = 'Carlos', 'Espinosa', 'Mexico'
print(nombre)
print(apellido)
print(pais)
```

## Pedir datos al usuario

La función `input` nos permite pedir datos al usuario y asignarlas a variables. Hay que tener en cuenta que los datos guardados de esta forma siempre serán **strings**.

```python
nombre = input('Cual es tu nombre? ')
edad = input ('Cual es tu edad? ')
print(nombre)
print(edad)
```

# Tipos de datos

Como ya se dijo anteriormente, en Python existen varios tipos de datos. Para verificar un tipo de dato podemos usar la función `type`. Una de las cosas más importantes de aprender un lenguaje de programación es entender los diferentes tipos de datos. A partir de aquí nos enfocaremos estudiar los tipos de datos.

## Revisando tipos de datos

- Para revisar un tipo de dato usamos la función `type`:
 
```python
nombre = 'Carlos'
edad = 100
print(type('Carlos'))
print(type(nombre))
print(type(10))
print(type(3.14))
print(type(1 + 1j))
print(type(True))
print(type([1,2,3,4,5]))
print(type({'nombre':'Carlos', 'edad':100, 'dato_random':True}))
print(type((1,2)))
print(type(zip([1,2],[3,4])))
```

- *Casting*: Podemos convertir un tipo de dato a otro (con ciertas restricciones). Para esto usaremos las funciones `int()`, `float()`, `str()`, `list`, `set`. Recuerden que siempre deben realizar operaciones entre datos del mismo tipo. Además, también deben de verificar los tipos de datos que están usando.

```python
# int a float
num_int = 10
print('num_int',num_int)         # 10
num_float = float(num_int)
print('num_float:', num_float)   # 10.0

# float a int
pi = 3.14
print(int(pi))                   # 3

# int a str
num_int = 10
print(num_int)                  # 10
num_str = str(num_int)
print(num_str)                  # '10'

# str a int o float
num_str = '10.6'
print('num_int', int(num_str))      # 10
print('num_float', float(num_str))  # 10.6

# str a list
nombre = 'Carlos'
print(nombre)                       # 'Carlos'
nombre_list = list(nombre)
print(nombre_list)            # ['C', 'a', 'r', 'l', 'o', 's']
```

# Números

Los tipos de datos clasificados como números en Python incluyen:

1. Enteros (**int**egers): Números enteros: ... -3, -2, -1, 0, 1, 2, 3, ...

2. Números de punto flotante (Números decimales, **float**): ..., -3.5, -2.25, -1.0, 0.0, 1.1, 2.2, 3.5, ...`

3. Números complejos: 1 + j, 2 + 4j, 1 - 1j
