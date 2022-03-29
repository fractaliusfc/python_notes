 # Funciones

 Hemos visto algunas de las funciones (métodos) que existen en Python, pero también podemos definir nuestras propias funciones.

 ## Qué es una función?

 Una función es un bloque de código reusable que está hecho para realizar cierta tarea. Para definir o declarar una función en python, usaremos el comando `def`.

## Declarando y llamando una función

Cuando hacemos una función, se le conoce que la estamos *declarando*. Cuando se usa una función, se dice que la estamos *llamando* o *invocando*.

## Parámetros de una función

### Función sin parámetros

Una función puede ser declarada sin parámetros.

```python
# Declaramos la funcion
def nombre_completo():
    nombre = 'Carlos'
    apellido = 'Espinosa'
    espacio = ' '
    nombre_c = nombre + espacio + apellido
    print(nombre_c)

# Llamamos la funcion
nombre_completo()
```

### Función regresando un valor

Una función puede regresar datos con el comando `return`. Por ejemplo, el nombre del ejemplo anterior o incluso un numero.

```python
def nombre_completo():
    nombre = 'Carlos'
    apellido = 'Espinosa'
    espacio = ' '
    nombre_c = nombre + espacio + apellido
    return nombre_c
```

```python
def suma_numeros():
    num1 = 2
    num2 = 3
    suma = num1 + num2
    return suma
print(suma_numeros())
```

### Función con parámetros

Una función puede recibir parámetros de cualquier tipo de datos.

```python
def saludos(nombre):
    mensaje = f"Hola {nombre}"
    return mensaje
```

```python
def numero_cuadrado(num):
    cuadrado = num * num
    return cuadrado
```

```python
def area_circ(r):
    PI = 3.1415
    area = PI * r * r
    return area
```

```python
def suma_numeros(n):
    resultado = 0
    for i in range(n+1):
        resultado += i
    print(resultado)
```

```python
def suma_numeros(num1, num2):
    suma = num1 + num2
    return sum
```

```python
def peso_objeto(masa, gravedad):
    peso = mass * gravedad
    return peso
```

### Usando el nombre de los parámetros

Podemos usar el nombre de los parámetros para que no importe el orden de los argumentos.

```python
def peso_objeto(masa, gravedad):
    peso = mass * gravedad
    return peso
print(peso_objeto(10, 9.81))
print(peso_objeto(gravedad=9.81, masa=5))
```

### El comando return (2da parte)

Si no regresamos ningún valor, la función regresará el valor `None` por defecto. 

```python
def peso_objeto(masa, gravedad):
    peso = mass * gravedad
    
def peso_objeto2(masa, gravedad):
    peso = mass * gravedad
    return peso
print(peso_objeto(10, 9.81))
print(peso_objeto2(5, 9.81))
```

### Función con parámetros por defecto

Algunas veces algunos parámetros no cambiarán en la mayoría de los casos, pero que es conveniente tenerlo como parámetros. En este tipo de casos es conveniente darles un valor por defecto.

```python
def peso_objeto(masa, gravedad=9.81):
    peso = mass * gravedad
    return peso
print(peso_objeto(10))
```

### Función como parámetro de otra función

Las funciones son tan versátiles que aceptan como parámetro otra función.

```python
def num_cuadrado(n):
    return n * n

def hacer_algo(f, x):
    return f(x)

print(hacer_algo(num_cuadrado, 3))
```
