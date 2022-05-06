# Clases y objetos

Python es un lenguaje de programación orientado a objetos. Todo en Python es un **objeto**, con sus respectivas propiedades y métodos. Un número, una string, una lista, un diccionario, una tupla, etc. usado en un programa es un objeto con una **clase** *built-in* correspondiente. Se necesita crear una clase para crear un objeto. Una clase es un constructor de objetos. Por lo que nosotros instanciamos una clase para crear un objeto. La clase define los atributos y el comportamiento del objeto, mientras que el objeto representa una clase.

Hemos estado trabajado con clases y objetos desde las primeras sesiones en que trabajamos con python.

```python
num = 10
type(num)

lst = []
type(lst)

dct = {}
type(dct)
```

## Creando una clase

Para crear una clase, necesitamos usar el comando `class` seguido de un nombre:

```python
class nombre_clase:
    # Codigo
```

Por ejemplo:

```python
class persona:
    pass
print(persona)
```

## Creando un objeto:

Creemos un objeto usando la clase definida antes:

```python
p = persona()
print(p)
```

## Clase constructora

En los ejemplos de arriba hemos creado un objeto a partir de la clase `persona`. Sin embargo, una clase sin un constructor no es muy útil para aplicaciones reales. Vamos a usar la función constructora para hacer nuestra clase más útil. En python usaremos la función constructora `init()`. La función constructora `init` tiene como parámetro `self` que es una referencia a la instancia actual de la clase:

```python
class persona:
    def __init__(self, nombre):
        self.nombre = nombre

p = persona('Carlos')
print(p.nombre)
print(p)
```

Agreguemos más parámetros a la función constructora:

```python
class persona:
    def __init__(self, nombre, apellido, edad):
        self.nombre = nombre
        self.apellido = apellido
        self.edad = edad

p = persona('Carlos', 'Espinosa', 100)
print(p.nombre)
print(p.apellido)
print(p.edad)
```

## Métodos de los objetos

A las funciones que son parte de una clase/objeto son llamadas **métodos**.

```python
class persona:
    def __init__(self, nombre, apellido, edad):
        self.nombre = nombre
        self.apellido = apellido
        self.edad = edad

    def info_persona(self):
        return f'{self.nombre} {self.apellido} tiene {self.edad} años'

p = persona('Carlos', 'Espinosa', 100)
print(p.info_personal())
```

## Valores por defecto en una clase

A veces es necesario tener valores por defecto para los métodos del objeto. Al igual como lo haciamos con las funciones, podemos tener valores por defecto en los parámetros del constructor.

```python
class persona:
    def __init__(self, nombre='Carlos', apellido='Espinosa', edad=100):
        self.nombre = nombre
        self.apellido = apellido
        self.edad = edad

    def info_persona(self):
        return f'{self.nombre} {self.apellido} tiene {self.edad} años'

p1 = persona()
print(p1.info_personal())
p2 = persona(nombre='Alejandra', apellido='Lugo', edad=101)
print(p2.info_personal())
```

## Herencia

Una propiedad interesante de las clases es la herencia. Esto significa que podemos reusar el código de una clase para definir una nueva clase que herede todos los métodos y propiedades de la clase *padre*. La clase padre (también llamada clase *super*, de superior, o *base*) es la clase donde se definen todos los métodos y propiedades. La clase *hija* es la clase que hereda todo de otra clase.

```python
class estudiante(persona):
    pass

est1 = estudiante('Lia', 'Flanders', '19')
print(est1.print())
```

Tengamos otro ejemplo:

```python
class animal():
    def __init__(self):
        print("Un animal ha sido creado")
    
    def que_eres(self):
        print("Soy un animal")
    
    def dormir(self):
        print("Durmiendo")

ani1 = animal()
ani1.dormir()
```

Hagamos una nueva clase heredando los elementos de la clase base. Hagamos una clase *gato*.

```python
class gato(animal):
    def __init__(self):
        animal.__init__(self)
        print('Un gato a sido creado')
    
    def que_eres(self):
        print("Soy un gato")

    def maullar(self):
        print("Miau")

suertudo = gato()
suertudo.que_eres()
suertudo.maullar()
```

## Polimorfismo

El polimorfismo en programación se refiere a la manera en que diferentes clases y objetos puedes compartir el mismo nombre de un método. Creemos dos clases, una de *perro* y otra de *gato* que van a tener el mismo método **hablar**. Cuando creamos el método `hablar`, este regresará un resultado único del objeto.

```python
class perro():
    def __init__(self, nombre):
        self.nombre = nombre

    def hablar(self):
        return self.nombre + " dice guau"

class gato():
    def __init__(self, nombre):
        self.nombre = nombre

    def hablar(self):
        return self.nombre + " dice miau"

p1 = perro("Lucas")
g1 = gato("Mina")

print(p1.hablar())
print(g1.hablar())
```
