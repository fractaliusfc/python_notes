# Conjuntos (sets)

Un conjunto en python es una colección de elementos sin ningún orden en particular. Generalmente en python se usan para guardar elementos únicos.

## Creando un conjunto

Para crear un conjunto, podemos usar las llaves (`{}`) o con la función `set()`

```python
set1 = {}
set2 = set()
```

Al igual que las listas y las tuplas, podemos crear un conjunto con sus elementos iniciales.

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
```

## Número de elementos

Al igual que con las listas y las tuplas, podemos recuperar el número de elementos con la función `len()`

```
frutas = {'limon', 'manzana', 'mango', 'platano'}
print(len(frutas))
```

## Accediendo a los elementos en un conjunto

Dado que no tenemos índices, la única manera de poder acceso a los elementos es mediante **ciclos**, pero esto lo veremos cuando lleguemos a este tema.

## Revisando si un elemento está en el conjunto

Podemos usar el operador `in` para revisar si un elemento se encuentra en el conjunto

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
print('limon' in frutas)
```

## Agregando elementos a los conjuntos

Una vez que el conjunto es creado, no podemos cambiar sus elementos. Sin embargo podemos agregar elementos adicionales.

Para esto, podemos usar el método `add()` si queremos agregar solo un elemento.

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
print(frutas)
frutas.add('naranja')
print(frutas)
```

Si queremos agregar multiples elementos, podemos usar el método `update()`. El argumento de este método será una **lista**.

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
print(frutas)
frutas.update(['naranja', 'tomate', 'pera'])
print(frutas)
```

## Borrando elementos de un conjunto

Podemos borrar un elemento de un conjunto con el método `remove()`. Si un elemento no está en el conjunto, este método nos dará como resultado un error. Siempre es bueno saber si el elemento está en el conjunto antes de tratar de borrarlo.

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
print(frutas)
frutas.remove('naranja')
print(frutas)
```

El método `pop()` eliminará un elemento al azar.

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
print(frutas)
frutas.pop()
print(frutas)
```

## Limpiando los elementos en un conjunto

Es posible *limpiar* un conjunto usando el método `clear()`

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
print(frutas)
frutas.clear()
print(frutas)
```

## Borrando un conjunto

Podemos borrar un conjunto usando el operador `del`

```python
frutas = {'limon', 'manzana', 'mango', 'platano'}
print(frutas)
del frutas
```

## Convertir una lista a un conjunto

Podemos convertir una lista a un conjunto y viceversa. Si convertimos a un conjunto una lista con elementos repetidos, estos elementos repetidos se eliminarán y solo se dejará uno.

```python
frutas_lst = ('limon', 'manzana', 'mango', 'platano', 'limon')
print(frutas_lst)
frutas_set = set(frutas_lst)
print(frutas_set)
```

## Uniendo conjuntos

Podemos unir dos conjuntos usando los métodos `union()` o `update()`

```python
frutas1 = {'limon', 'manzana'}
frutas2 = {'mango', 'platano'}
frutas = frutas1.union(frutas2)
print(frutas)
```

```python
frutas1 = {'limon', 'manzana'}
frutas2 = {'mango', 'platano'}
frutas = frutas1.update(frutas2)
print(frutas)
```

## Encontrando la intersección de dos conjuntos

Podemos encontrar los elementos en común de dos conjuntos dados con el método `intersection()`

```python
frutas1 = {'limon', 'manzana', 'mango', 'platano'}
frutas2 = {'pera', 'manzana', 'mango', 'tomate'}
frutas1.intersection(frutas2)
```

## Revisando si un subconjuntos

Un conjunto puede ser un subconjunto o un superconjunto de otros subconjuntos. Para esto se usan los métodos `issubset()` y `issuperset()`.

```python
numeros = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
numeros_pares = {0, 2, 4, 6, 8, 10}
numeros.issubset(numeros_pares)
numeros.issuperset(numeros_pares)
```

## Revisando la diferencia entre dos conjuntos

El método `difference` nos dará como resultado la diferencia entre dos conjuntos.

```python
numeros = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
numeros_pares = {0, 2, 4, 6, 8, 10}
numeros.difference(numeros_pares)

python = {'p', 'y', 't', 'h', 'o','n'}
dragon = {'d', 'r', 'a', 'g', 'o','n'}
python.difference(dragon)    
dragon.difference(python)     
```

## Diferencia simétrica entre dos conjuntos

La diferencia simétrica es un conjunto que contiene los elementos de ambos conjuntos excepto aquellos que están en ambos conjuntos.

```python
numeros = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
algunos_numeros = {1, 2, 3, 4, 5}
numeros.symmetric_difference(algunos_numeros)

python = {'p', 'y', 't', 'h', 'o','n'}
dragon = {'d', 'r', 'a', 'g', 'o','n'}
python.symmetric_difference(dragon) 
```

## Conjuntos disjuntos

Si dos conjuntos no tienen elementos en común se les dice conjuntos disjuntos. Podemos revisar esto con el método `isdisjoint()`.

```python
numeros pares = {0, 2, 4 ,6, 8}
numeros_impares = {1, 3, 5, 7, 9}
numeros_pares.isdisjoint(numeros_impares)

python = {'p', 'y', 't', 'h', 'o','n'}
dragon = {'d', 'r', 'a', 'g', 'o','n'}
python.isdisjoint(dragon)
```
