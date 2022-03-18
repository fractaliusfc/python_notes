# Tuplas

Una tupla es una colección de diferentes tipos de datos con un orden en específico y que son **inmutables**. Las tuplas son definidas con **paréntesis**. Este tipo de colección no puede ser modificada una vez que se ha creado, es decir, no se pueden agregar, insertar o eliminar elementos.

## Creando una tupla

Una tupla puede crearse entera por medio de los siguientes comandos

```python
tupla_vacia = ()
tupla_vacia = tuple()
```

Al igual que las listas, las tuplas pueden ser definidas con sus elementos:

```python
tupla = (1, 2, 3, 4, 5)
```

## Número de elementos en una tupla

Al igual que los otras colecciones de elementos, se puede conocer el número de elementos con la función `len()`

```python
tupla = (1, 2, 3, 4, 5)
num_elementos = len(tupla)
print(num_elementos)
```

## Accediendo a los elementos de una tupla

Al igual que las listas, las tuplas son una colección de elementos ordenados, esto significa que se les asigna un índice a los elementos.

```python
frutas = ('limon', 'manzana', 'mango', 'platano')
primera_fruta = frutas[0]
print(primera_fruta)
segunda_fruta = frutas[1]
print(segunda_fruta)
```

Al igual que las listas, también se pueden usar índices negativos.

```python
frutas = ('limon', 'manzana', 'mango', 'platano')
ultima_fruta = frutas[-1]
```

## Creando subtuplas

Al igual que en las listas, podemos crear sub tuplas índicando los índices correspondientes.

```python
frutas = ('limon', 'manzana', 'mango', 'platano')
toda_frutas = frutas[0:]
manzana_mango = frutas[1:3]
manaza_y_resto = frutas[1:]
```

## Transformando tuplas a listas

Es posible cambiar tuplas a listas y listas a tuplas. Una tupla es *inmutable*, pero si queremos modificarla, podemos cambiarla a una lista.

```python
frutas_tpl = ('limon', 'manzana', 'mango', 'platano')
frutas_tpl[0] = 'naranja'    # Error
frutas_lst = list(frutas_tpl)
frutas_lst[0] = 'naranja'
print(frutas_lst)
frutas = tupla(frutas_lst)
print(frutas)
```

## Revisando si un elemento está en una tupla

Podemos revisar si cierto elemento se encuentra en una lista con el operador `in`.

```python
frutas = ('limon', 'manzana', 'mango', 'platano')
print('naranja' in frutas)
print('mango' in frutas)
```

## Uniendo tuplas
Podemos unir dos tuplas usando el operador `+`.

```python
frutas1 = ('limon', 'manzana')
frutas2 = ('mango', 'platano')
frutas = frutas1 + frutas2
```

## Borrando tuplas

Dado que no se pueden eliminar elementos de una tupla, la único que podemos hacer es borrar toda la tupla.

```python
frutas = ('limon', 'manzana', 'mango', 'platano')
del frutas
```
