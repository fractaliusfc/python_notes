# Notacion Big-O y análisis de algoritmos

En programación hay distintas maneras de resolver un problema. Por ejemplo, hay distintas maneras de ordenar una lista de elementos. Algunos métodos de ordenamiento son:

- Merge Sort
- Bubble Sort
- Insertion Sort

Todos estos algoritmos tienes sus ventajas y desventajas. Entonces, qué algoritmo se debe de usar para resolver un problema en específico cuando hay multiples soluciones al problema?

El análisis de algoritmos se refiere a analizar la complejidad de diferentes algoritmos y encontrar el algoritmo más eficiente para resolver el probrema. La notación Big-O es una medida estadística para describir la complejidad de un algoritmo.

## Por qué es importante en análisis de un algoritmo?

Supongamos el siguiente ejemplo: supongamos que un supervisor le da una tarea a dos de sus empleados para diseñar un algoritmo en Python que calcule el factorial de un número dado.

Uno de los dos empleados desarrolla el siguiente algoritmo:

```python
def fact(n):
    prod = 1
    for i in range(n):
        prod = prod * (i + 1)
    return product

print(fact(5)) 
```

Podemos ver que el algoritmo toma un entero como argumento. En la función `fact`, la variable prod será la encargada de guardar el producto y por lo tanto inicia en 1. El ciclo for se ejecuta desde 1 a `n` y, durante cada iteración. el valor del prod es multiplicado por el número que está siendo iterado por el ciclo. El resultado es guardado en `prod` una y otra vez. Al final de ciclo, la variable `prod` es guardada en el factorial.

Igualmente, el segundo empleado desarrolla un algoritmo que calcula el factorial de un número. El segundo empleado usa una función *recursiva* para calcular el factorial.

```python
def fact2(n):
    if n == 0:
        return 1
    else:
        return n * fact2(n-1)
print(fact5(5))
```

El supervisor tiene que decidir que algoritmo usar. Para hacer eso, analiza ambos algoritmos para encontrar la complejidad deada uno. Una manera de hacer esto es encontrando el tiempo en que se ejecutarán ambos algoritmos.

En un `Ipython` o `Jupyter Notebook`, podemos usar `%timeit` para encontrar el tiempo de ejecución.

```python
%timeit fact(50)
```

Por lo que analizando el tiempo de ejecución, podremos encontrar que algoritmo es mejor. Sin embargo, el tiempo de ejecución no es una buena métrica para medir la complejidad de un algoritmo ya que depende del *hardware*. Por lo que se necesita una métrica mas objetiva para medir la complejidad de una algoritmo.

## Analizando un algoritmo con notación Big-O

La notación Big-O es una métrica usada para encontrar la complejidad de un algoritmo. Básicamente, esta notación es la relación entre la entrada del algoritmo y los pasos realizados por el algoritmo. Se utiliza una O mayúscula seguido por paréntesis. Dentro de los paréntesis, se escribe la relación entre la entrada y los pasos dados por el algoritmo usando la letra n.

Podemos encontrar los siguientes tipos de complekidad


Nombre   | Big O 
---------|----------
 Constante | O(c)    
 Lineal | O(n)
 Cuadrático | O(n^2) 
 Cúbico | O(n^3) 
 Exponencial | O(2^n) 
 Logarítmico | O(log(n)) 
 Lineal Log | O(nlog(n))

 Para tener una idea de como se calcula la complejidad usando la notación Big-O, veamos algunos ejemplos.

### Complejidad Constante (O(c))

La complejidad de un algoritmo es constante si los pasos requeridos para completas la ejecución de un algoritmo son siempre constantes sin importar el número de entrada. La notación utiliza para este tipo de complejidad es O(c).

Vamos a escribir un programa sencillo con este tipo de complejidad.

```python
def algo_constant(items):
    resultado = items[0] * items[0]
    print(resultado)

algo_constant([4,5,6,8])
```

En el script anterior, el número de pasos es siempre constante sin importar el número de elementos de la lista `items`. Por lo tanto, la complejidad permanece constante.

### Complejidad linea (O(n))

La complejidad de un algoritmo es lineal si los pasos requeridos para completar un algoritmo incrementan (o decrecen) linealmente con el número de entradas. Este tipo de complejidad es denotada con O(n)

Por ejemplo, tomemos el siguiente programa:

```python
def algo_lineal(items):
    for item in items:
        print(item)
algo_lineal([4,5,6,8])
```

La complejidad de esta función es lineal, dado que el número de iteraciones del ciclo for será igual al tamaño de la lista de entrada `items`. Por lo que si hay 4 elementos, el ciclo for tendrá 4 iteraciones. Si hay 10 elementos, el ciclo for tendrá 10 iteraciones.
