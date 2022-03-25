# Ciclos

La repetición o rutinas diarias nos acompañan en nuestro día a día. En programación existen bastantes tareas repetitivas con las cuales tenemos que lidiar día con día. Para manejar estas tareas se usan ciclos iterativos o *loops*. En Python encontraremos dos tipos de ciclos:

- Ciclo `while`
- Ciclo `for`

## Ciclo while

El ciclo while se caracteriza por ejecutar repetidamente un bloque de código mientras una condición dada sea verdadera. Cuando esta condición ya no es verdadera, el ciclo se detendrá y el programa continuará con las líneas de códigos colocadas después del ciclo. El comando para usar este tipo de ciclo es `while`.

```python
contador = 0
while contador < 5:
    print(contador)
    contador = contador + 1
```

En el ciclo while anterior, la condición ya no se cumple cuando el contador alcanza el valor de 5. En este momento el ciclo para. Si nos interesa correr un bloque de código especial una vez que la condición ya no se cumple, podemos usar `else`.

```python
contador = 0
while contador < 5:
    print(contador)
    contador = contador + 1
else:
    print(contador)
```

En el ciclo while anterior, el ciclo parará cuando contador sea 5. En ese momento se ejecutará el bloque de código bajo el comando `else`, en este caso se imprimirá el valor de la variable contador.

### break y continue (Parte 1)

En algunas ocasiones necesitaremos forzar que el ciclo pare, para este caso tenemos el comando `break`.

```python
contador = 0
while contador < 5:
    print(contador)
    contador = contador + 1
    if contador == 3:
        break
```

En el ciclo while anterior solo se mostraran los valores 0, 1 y 2. Cuando la variable contador tome el valor 3, el ciclo se *romperá*.

Por otra parte, también podemos tener la necesidad de saltarnos cierta iteración, para esto tenemos el comando `continue`.

```python
contador = 0
while contador < 5:
    if contador == 3:
        contador = contador + 1
        continue
    print(contador)
    contador = contador + 1
```

En el ciclo while anterior solo mostrará 0, 1, 2 y 4, cuando el contador sea igual a 3 saltará los siguientes comandos.

## Ciclo for

Un ciclo for es usado para iterar sobre una secuencia de elementos (listas, tuplas, diccionarios, conjuntos o strings). El comando para usarlo es `for`.

```python
numeros = [0, 1, 2, 3, 4, 5]
for numero in numeros:
    print(numero)
```

```python
palabra = 'python'
for letra in palabra:
    print(letra)
```

```python
numeros = (0, 1, 2, 3, 4, 5)
for numero in numeros:
    print(numero)
```

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
for fruta in frutas:
    print(fruta)
```

```python
persona = {
    'nombre1': 'Carlos',
    'nombre2': 'Crispin',
    'edad': 32,
    'pais': 'Mexico',
    'licenciatura': True,
    'habilidades': ['C', 'C++', 'python', 'fortran', 'markdown', 'latex'],
    'direccion': {
        'calle': 'Calle Falsa',
        'numero': 123,
        'cp': 20123
    }
}

for key in persona:
    print(key)

for key, valor in persona.items():
    print(key, valor)
```

### break y continue (Parte 2)

Al igual que con el ciclo while, en el ciclo for podemos usar `break` para parar el ciclo antes de que termine.

```python
numeros = (0, 1, 2, 3, 4, 5)
for numero in numeros:
    print(numero)
    if numero == 3:
        break
```

Se usará `continue` para saltar a la siguiente iteración del ciclo:

```python
numeros = (0, 1, 2, 3, 4, 5)
for numero in numeros:
    if numero == 3:
        continue
    print(numero)
```

### La función range

La función `range` nos permitirá crear listas de números. Esta función toma tres parámetros, `range(start, end, step)`. El primero, *start*, nos permitirá decidir el número inicial (por defecto, este es 0). El segundo, *end* nos permitirá definir hasta donde queremos la lista de números (se aplica la regla de que no *tocará* el último número). Finalmente, *step* definirá el incremente en nuestra lista de números (por defecto es 1).

```python
lista_range = range(11)
print(lista_range)
lista = list(range(11))
print(lista)
lista2 = list(range(0,11,2))
print(lista2)
```

Su mayor ventaja es poder usarlo en el ciclo for directamente.

```python
for numero in range(11):
    print(numero)
```

### Ciclos anidados

Al igual que paso con el condicional `if`, puede llegar el caso en que necesitemos un ciclo dentro de otro ciclo.

```python
persona = {
    'nombre1': 'Carlos',
    'nombre2': 'Crispin',
    'edad': 32,
    'pais': 'Mexico',
    'licenciatura': True,
    'habilidades': ['C', 'C++', 'python', 'fortran', 'markdown', 'latex'],
    'direccion': {
        'calle': 'Calle Falsa',
        'numero': 123,
        'cp': 20123
    }
}

for key in persona:
    if key == 'habilidades':
        for habilidad in persona['habilidades']:
            print(habilidad)
```

### For else

En el ciclo for también es posible usar el comando `else`. Este se utilizará si se quiere ejecutar algún bloque de código cuando el ciclo termine.

```python
for numero in range(11):
    print(numero)
else:
    print(f'El loop ha terminado, la variable número es {numero}')
```

## Pass

En muchos comandos de python es requerido poner algún comando después de los dos puntos. Sin embargo, en diversos motivos no queremos que se ejecute ningún código. Para este tipo de casos existe el comando `pass` para evitar algún tipo de errores. También puede ser usado para dejar en *stand by* cierta parte del código.

```python
for numero in range(7):
    pass
```
