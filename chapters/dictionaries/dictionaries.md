# Diccionarios

Un diccionario es una colección de elementos **no ordenada** y **mutable** por **pares** (*key*:*valor*).

Todos los datos en un diccionario están en parejas de datos: una de ellos servirá como identificador (key) y el otro será el dato asociado a ese identificador.

## Creando un diccionario

Para crear un diccionario se puede usar la función `dict()` o las llaves `{}`.

```python
diccionario_vacio = {}
```

También se puede definir con sus valores iniciales.

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
```

Los diccionarios pueden guardar cualquier tipo de dato.

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
```

## Tamaño de un diccionario

El tamaño de un diccionario será igual a cada una de las parejas *key*:*dato* que contenga. Se puede revisar con la función `len()`

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
print(len(dcr))
```

## Accediendo a los elementos de un diccionario

Podemos acceder a los elementos de un diccionario usando directamente la *key* de los elementos.

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
print(dcr['id1'])
print(dcr['id4'])
```

Otro ejemplo

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

print(persona['nombre1'])
print(persona['pais'])
print(persona['habilidades'])
print(persona['habilidades'][2])
print(persona['direccion']['calle'])
print(persona['internet'])    # Error  
```

Su uno trata de accesar a un dato cuya *key* no exista, python dará un error diciendo que la *key* no existe. Para evitar este error se debe revisar primero si la llave existe o usar el método `get()`. Este método dará como resultado `None` si no existe la *key*.

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

print(persona.get('nombre1'))
print(persona.get('pais'))
print(persona.get('habilidades'))
print(persona.get('direccion'))
print(persona.get('internet'))    # Error  
```

## Agregando elementos a un diccionario

Podemos  agregar elementos a un diccionario especificando la *key* y el valor asociado.

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

persona['materia'] = 'MNyAC'
```

## Modificando elementos en un diccionario

Modelos modificar los elementos de un diccionario de la misma manera, dando la *key* correspondiente y el nuevo valor.

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

persona['edad'] = 30
persona['nombre1'] = 'Solrac'
```

## Revisando si existe una key en un diccionario

Se usa el operador `in` para revisar si una key existe en un diccionario.

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
print('id2' in dcr)
print('id5' in dcr)
```

## Eliminando key y valores de un diccionario

Podemos eliminar elementos de un diccionario usando los siguientes métodos:

- `pop(key)`: Elimina el elemento de la key dada.
- `poptiem()`: Elimina el último elemento
- `del`: Elimina el elemento de la key especificada.

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

persona.pop('nombre1')
persona.popitem()
del persona['pais']
```

## Transformando un diccionario a una lista

Podemos cambiar un diccionario a una lista de los elementos de un diccionario por medio del método `items()`.

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
print(dcr.items())
```

## Limpiando un diccionario

Podemos borrar todos los elementos de un diccionario con el método `clear()`

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
print(dcr.clear())
```

## Borrando un diccionario

Podemos borrar un diccionario completamente con el comando `del`

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
del dcr
```

## Copiando un diccionario

Podemos copiar un diccionario usando el método `copy()`.

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
dcr_copia = dcr.copy()
```

## Obteniendo las keys de un diccionario como una lista.

Podemos obtener todas las keys de un diccionario como una lista con el método `keys()`.

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
keys = dcr.keys()
print(keys)
```

## Obteniendo los valores de un diccionario como una lista.

Podemos obtener todos los valores de un diccionario como una lista con el método `values()`.

```python
dcr = {'id1':'valor1', 'id2':'valor2', 'id3':'valor3', 'id4':'valor4', 'id5':'valor5'}
valores = dcr.values()
print(values)
```
