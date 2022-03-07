# Strings

El texto, o conjunto de caracteres, es un tipo de dato llamado `string`. Cualquier tipo de dato escrito como texto es una `string`. Cualquier tipo de dato entre comillas simples, dobles o triples serán tratados como una `string`. Hay varias funciones que nos sirven para usar las `string`, por ejemplo la función `len()`:

## Creando una string

```python
letra = 'H'
print(letra)
print(len(letra))
saludos = 'Hola, Mundo'
print(saludos)
print(len(saludos))
enunciado = "Esta es la clase de Metodos Numericos y Algoritmos Computacionales"
print(enunciado)
```

Las `string` multilineas se definen usando triple comillas simple (`'''`) o triple comillas dobles (""").

```python
string_multilinea = '''The impression I had was that we were leaving the West and entering the East; the most western of splendid bridges over the Danube, which is here of noble width and depth, took us among the traditions of Turkish rule.'''
print(string_multilinea)

string_multilinea_2 = """Having had some time at my disposal when in London, I had visited the British Museum, and made search among the books and maps in the library regarding Transylvania; it had struck me that some foreknowledge of the country could hardly fail to have some importance in dealing with a nobleman of that country."""
print(string_multilinea_2)
```

## Concatenación de strings

Podemos unir dos strings. Combinar o conectar dos strings es llamado concatenación.

```python
nombre = 'Carlos'
apellido = 'Espinosa'
spacio = ' '
nombre_completo = nombre + spacio + apellido
print(nombre_completo)
# Revisando el tamaño de las strings usando len()
print(len(nombre))
print(len(apellido))
print(len(nombre) > len(apellido))
print(len(nombre_completo))
```

## Secuencias de escape de strings

En los lenguajes de programación existen secuencias de escape que funcionan para agregar ciertos caracteres especiales o funciones. Estas secuencias se ponen con el caractér `\` seguido por una letra. Los más comunes son enlistados a continuación

- `\n`: nueva línea
- `\t`: Tabulación
- `\\`: Diagonal
- `\'`: Comilla simple
- `\"`: Comillas dobles

Ejemplos:

```python
print('Hola \nMundo')
print('Buenas\ttardes\tCarlos')
print('Esta es la manera de escribir una diagonal (\\)')
print('El primer programa inicia con \"Hola Mundo\"')
```

## Formateo de Strings

### Estilo Clásico (Operador %)

En python existen distintas maneras de darle cierto formato a las `strings`. El operador `%` es usado para usar un conjunto de variables en una string. Al usar este operador, se tiene que especificar el tipo de variable y/o numero de digitos que uno quiere obtener. 

- %s Se usa para strings o cualquier cosa que se pueda representar con strings
- %d Para enteros
- %f Para decimales
- %.numero_de_digitosf Número de decimales

Ejemplos

```python
nombre = 'Carlos'
apellido = 'Espinosa'
lenguaje = 'Python'
string_format1 = 'Hola, soy %s %s. Estamos aprendiendo %s' %(nombre, apellido, lenguaje)
print(string_format1)

radio = 10
pi = 3.14
area = pi * radio ** 2
string_format2 = 'El area de un circulo con un radio %d es %.2f.' %(radio, area)
print(string_format2)
```

### Estilo nuevo (str.format)

Este estilo fue introducido con Python 3

```python
nombre = 'Carlos'
apellido = 'Espinosa'
lenguaje = 'Python'
string_format3 = 'Hola soy {} {}. Estamos aprendiendo {}'.format(nombre, apellido, lenguaje)
print(string_format3)

a = 4
b = 3

print('{} + {} = {}'.format(a, b, a + b))
print('{} - {} = {}'.format(a, b, a - b))
print('{} * {} = {}'.format(a, b, a * b))
print('{} / {} = {:.2f}'.format(a, b, a / b))
print('{} % {} = {}'.format(a, b, a % b))
print('{} // {} = {}'.format(a, b, a // b))
print('{} ** {} = {}'.format(a, b, a ** b))

radio = 10
pi = 3.14
area = pi * radio ** 2
string_format4 = 'El area de un circulo con un radio {} es {:.2f}'.format(radio, area)
print(string_format4)
```

### f-strings

En las nuevas versiones de Python (3.6+) se incluyo las llamadas **f-strings**. Este método se caracteriza por `strings` iniciando con `f` y teniendo una sintaxis similar al estilo anterior.

```python
a = 4
b = 3

print(f'{a} + {b} = {a + b}')
print(f'{a} - {b} = {a - b}')
print(f'{a} * {b} = {a * b}')
print(f'{a} / {b} = {a / b:.2f}')
print(f'{a} % {b} = {a % b}')
print(f'{a} // {b} = {a // b}')
print(f'{a} ** {b} = {a ** b}')
```

## Strings como secuencia de caracteres

Otra forma de ver las `strings` en Python es como una secuencia de caracteres. La forma mas simple de extraer cada uno de los caracteres que forman una `string` es *desempaquetandolos* en distintas variables.

```python
lenguaje = 'Python'
a,b,c,d,e,f = languaje
print(a) # P
print(b) # y
print(c) # t
print(d) # h
print(e) # o
print(f) # n
```

### Accediendo a los caracteres por índice

A cada uno de los caracteres en un string se les asigna un *id* basado en su posición. A este *id* se le conoce como **índice**. En muchos lenguajes de programación, el índice empieza desde 0. Por lo tanto, la primera letra de una string tiene un índice 0, mientras que la última letra su índice es igual al número de caracteres menos 1.

![Índices en una string](./figures/string_index.png)

```python
lenguaje = 'python'
primera_letra = lenguaje[0]
print(primera_letra)
segunda_letra = lenguaje[1]
print(segundo_letra)
ultimo_indice = len(lenguaje) - 1
ultima_letra = lenguaje[ultimo_indice]
print(ultima letra)
```

También se puede empezar a contar de derecha a izquierda usando índices negativos, donde la ultima letra le corresponde el índice -1.

```python
lenguaje = 'python'
ultima_letra = lenguaje[-1]
print(ultima_letra)
segunda_ultima_letra = lenguaje[-2]
print(segunda_ultima_letra)
```

### Substrings de strings

Podemos obtener *substrings* a partir de una string:

```python
palabra = 'python'
primeras_tres = palabra[0:3] # Devuelve desde el indice 0 hasta el 3 sin incluir el 3
print(primeras_tres)
ultimas_tres = palabra[3:6]
print(ultimas_tres)
ultimas_tres_alt = palabra[-3:]
print(ultimas_tres)
ultimas_tres_alt2 = palabras[3:]
print(ultimas_tres)
```

### Substring saltando letras

Cuando definimos una substring, podemos especificar si queremos tener un salto diferente en los índices.

```python
palabra = 'Python'
substring = palabra[0:6:2]
print(substring)
```

### Invirtiendo una string

Podemos invertir una string de una manera sencilla

```python
saludo = 'Hola Mundo'
saludo_inv = saludo[::-1]
print(saludo_inv)
```

## Métodos de Strings

Los métodos son **funciones** que realizan una tarea especifica. En este caso veremos método que toman una string como argumento y realizan una tarea específica con ella. Hay bastantes métodos de strings, aquí solamente veremos algunos.

- `capitalize()`: Convierte el primer caracter de una string a mayúscula

```python
mensaje = 'metodos numericos y algoritmos computacionales'
print(mensaje.capitalize())
```

- `count()`: Regresa el numero de veces que una substring aparece en una string.

```python
mensaje = 'metodos numericos y algoritmos computacionales'
print(mensaje.count('m'))
print(mensaje.count('m', 17, 25))
print(mensaje.count('os'))
```

- `endswith()`: Revisa si la string termina con una determinada string

```python
mensaje = 'metodos numericos y algoritmos computacionales'
print(mensaje.endswith('les'))   # True
print(mensaje.endswith('le'))    # False 
```

- `strip()`: Elimina todos los caracteres especificados

```python
mensaje = 'metodos numericos y algoritmos computacionales'
print(mensaje.strip('met'))
```

- `split()`: Divide la string de acuerdo a otra string

```python
mensaje = 'metodos numericos y algoritmos computacionales'
print(mensaje.split('s'))
```

- `startswith()`: Revisa si una string inicia con una string especifica
```python
mensaje = 'metodos numericos y algoritmos computacionales'
print(mensaje.startswith('met'))   # True
print(mensaje.startswith('metu'))    # False 
```