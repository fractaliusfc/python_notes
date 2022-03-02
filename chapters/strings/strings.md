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
