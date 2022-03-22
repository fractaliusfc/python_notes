# Condicionales

En un script, los comandos son ejecutados secuencialmente desde inicio hasta el final. En Python se puede alterar esta secuencia de dos maneras.

- Ejecución condicional: Un bloque de comandos son ejecutados si cierta expresión se cumple.
- Ejecución repetitiva:un bloque de comandos será ejecutado de manera repetitiva mientras una condición se cumpla.

En esta sección se verán los comandos condicionales `if`, `else` y `elif`. Los operadores de comparación y lógicos serán usados en combinación con estos comandos.

## Condicional If

En python, y otros lenguajes de programación, el comando `if` es usado para ejecutar ciertas instrucciones si una condición se cumple. El bloque de comandos a ejecutar si la condición se cumple es definido por medio de la **indentación**.

```python
a = 3
if a > 0:
    print('a es un número positivo')
```

En este ejemplo, la condición se cumple dado que 3 es mayor que 0. Dado que la condición es cierta, el bloque de código indentado se ejecuta. Sin embargo, si la condición fuera falsa, podemos definir otro bloque de código que se puede ejecutar bajo el comando `else`.

## Condicional If Else

Si la condición de un `if` no se cumple, los comandos que estén bajo el comando `else` serán ejecutados.

```python
a = 3
if a < 0:
    print('a es un número negativo')
else:
    print('a es un número positivo')
```

Dado que la condición del `if` es falsa, el código bajo el comando `else` es ejecutado. Sin embargo, podemos definir una nueva condición para decidir si se ejecute un bloque de código en dado caso que la primera condición no se cumpla.

## Condicional If Elif Else

Generalmente, una decisión se basa en condiciones multiples. Se usa `elif` cuando tenemos mas de una condición.

```python
a = 0
if a > 0:
    print('a es un número positivo')
elif a < 0:
    print('a es un número negativo')
else:
    print('a es cero')
```

## Condicionales anidados

Podemos tener un `if` dentro de otro  `if`.

```python
a = 0
if a > 0:
    if a % 2 == 0:
        print('a es positivo y par')
    else:
        print('a es positivo')
elif a == 0:
    print('a es cero')
else:
    print('a es negativo')
```

Podemos evitar esta escritura *anidada* por usar operadores lógicos.

## Condicional If y operadores lógicos

### Operador and

```python
a = 0
if a > 0 and a % 2 == 0:
        print('a es positivo y par')
elif a > 0 and a % 2 !=  0:
     print('a es positivo')
elif a == 0:
    print('a es cero')
else:
    print('a es negativo')
```

### Operador or

```python
usuario = 'espinosa'
nivel_seguridad = 3
if usuario == 'admin' or nivel_seguridad >= 4:
    print('Acceso confirmado')
else:
    print('Acceso denegado')     
```
