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

También se puede empezar a contar de derecha a izquierda usando índices negativos. Donde -1 es el último índice

```python
lenguaje = 'python'
ultima_letra = lenguaje[-1]
print(ultima_letra)
segunda_ultima_letra = lenguaje[-2]
print(segunda_ultima_letra)
```
