# APUNTES DE LA SEGUNDA PARCIAL
## Programación Funcional 
<p><em><strong>Stringdocs:</strong></em> Las docstrings son las cadenas que aparecen justo después de la definición de una 
función, método, clase o módulo. Estas son usadas para documentar, como ya se dijo antes, un módulo, clase, 
función o método en Python. Cabe recalcar que se usan para que otros programadores entiendan fácil y rápidamente lo que hace esa parte del programa.</p>   
<p><em><code>def cubo(num):
    ''' Toma un número y regresa el cubo de dicho número'''
    return num**3
print(cubo.__doc__)</code></em>
<p>El docstring es lo que está entre las comillas triples y con .__doc__ se llama a dicha documentación.</p>
<p><em><strong>REPL:</strong></em> Repeat Evual Print Loop. </p>    
<p><em><strong>Lambda:</strong></em> Las funciones lambda también llamadas <em>funciones anónimas</em> son funciones simpres 
de una sola expresión que se pueden utilizar in situ. Cabe destacar que estas funciones no usan <em>return</em> y se limitan 
a una sola sentencia. También no es recomendable abusar de ellas porque hacen que el código sea menos legible.</p>  
<p><em><code>superficie = lambda alto, ancho: alto*ancho 
resultado = superficie(5,7)
print("La superficie es de: ",resultado)</code></em>
<p><em><strong>Args y Kwargs:</strong></em> Pueden ser puras (tiene argumentos, entre otras cosas) e impuras (no tiene argumentos, entre otras cosas).</p>  
<p><em><strong>Args:</strong></em> Cuando se quiere que una función acepte un número arbitrario de argumentos, se usan los "args".
Los *args son un parámetro que se define como cualquier otro, pero con un asterisco delante del nombre. Python interpretará esto 
como el nombre de una tupla en la que se almacenarán todos los argumentos que se reciben.</p> 
<p><em><code>def imprime_lista(nombre_lista, *cosas):
    print("Lista de " + nombre_lista)
    for cosa in cosas:
        print(cosa)
imprime_lista("Piezas","tornillo","cable","clavo","tuerca")</code></em></p>
<p><em><strong>Kwargs:</strong></em> Es la abreviación en inglés de "Keyword Arguments" y se trata de argumentos que se pasan 
por pares de <em>clave-valor</em> y se reciben como un diccionario. En lugar de un asterisco (como en los args), se usan dos.</p> 
<p><em><code>imprime_lista("Piezas","tornillo","cable","clavo","tuerca")

def imprime_datos(nombre, **datos):
    print("Datos de " + nombre)
    for clave in datos:
        print(clave + ": " + datos[clave])
imprime_datos("Pedro", edad = "19", estado = "feliz", alto = "sí")</code></em></p>  
<p><em><strong>Nota-> Si se usan argumetos fijos, *args y **kwargs, se deben poner en orden. Primero los fijos, luegos 
los *args y, al final, los **kwargs.</strong></em></p>  
<p><em><code>def imprimir_datos(nombre, *lista, **diccionario):
    print("Nombre: ", nombre)
    print("Lista:")
    for elemento in lista:
        print(" - ", elemento)
    print("Diccionario:")
    for clave, valor in diccionario.items():
        print(" - ", clave, ": ", valor)    
imprimir_datos("Un nombre", "argumento 1", "argumento 2", clave_1 = "valor 1", clave_2 = "valor 2")</code></em></p>
<hr>
<hr>
<p><strong>Funciones</strong></p>
<p><strong>->Introducción a las funciones</strong></p>

* Prácticamente todos los lenguajes de programación actuales permiten una forma de crear funciones definidas por el usuario.
* Cabe resaltar que no siempre se denominan funciones.
* En otros lenguajes pueden llamarse:
  * Subrutinas
  * Procedimientos
  * Métodos
  * Subprogramas
 
<p>En programación, una <em>función</em> es un bloque de código independiente para una tarea específica o un grupo de tareas relacionadas.</p>
Ejemplos:
  * id()
  * len()
  * max()
  * min()

<hr>

<p><strong>->Definición y ventajas de su uso</strong></p>

* Una función es una relación o mapeo entre una o más entradas y un conjunto de salidas.
* En matemáticas, una función normalmente se representa como $$ y = f(x)$$
* *f* es una función que opera sobre la entrada *x*
* La salida de la función es *y*

<hr>
 
<p><strong>->Declaración y llamada de funciones.</strong></p>

* Una función se declaran con la palabra reservada *def*
* Una función puede recibir parámetros
* Una función puede retornar un valor, varios o ninguno
* Cuando no retorna nada de manera explícita, siempre retorna *None*
* Una función puede ser recursiva
* Sintaxis general de una función:

``` python
def <function_name>([<parameters>]):
    <statement(s)>
```

Donde:
| Elemento        | Significado                                                                      |
|-----------------|----------------------------------------------------------------------------------|
|def              | Palabra clave para indicar que se está **def**iniendo una función                |
|<function_name>  | Un identificador de Python válido que nombra a la función                        |
|\<parameters>    | Lista opcional separada por comas de parámetros que se pueden pasar a la función |
|:                | Símbolo que indica el final del encabezado o firma de la función de Python       |
|<statement(s)>   | Bloque de sentencias válidas de Python                                           |

* Para llamar a la función:
``` python
<function_name>([<arguments>])
```
* <em>arguments</em> son los valores pasados a la función.
* Corresponden a los <parameters> en la definición de la función.
* Se puede definir una función que no acepte ningún argumento, pero los paréntesis aún son necesarios.
* Tanto una definición de función como una llamada a función siempre deben incluir paréntesis, aunque estén vacíos.
<p>Ejemplo de funciones en un código:</p>  
<p><strong>1</strong></p>
<p><code>def a():
    x = "Hola"
    print(x)
    
def b():
    x = "Hello"
    print(x)

x = "Hi"
print(x)
a()
b()</code></p>

<p><strong>2</strong></p>
<p><code>def mi_funcion():
    msg = "Dentro de mi_funcion"
    print(msg)

print("Antes de llamar a mi_funcion")
mi_funcion()
print("Despues de llamar a mi_funcion")</code></p>

<p><em><strong>Run: </strong></em></p>
<p>Antes de llamar a mi_funcion</p>
<p>Dentro de mi_funcion</p>
<p>Despues de llamar a mi_funcion</p>
<hr>
<p><strong>Parámetros y argumentos.</strong></p>

* Sintaxis de una función:

``` python
def <function_name>([<parameters>]):
    <statement(s)>
```

* Llamada de una función:

```python
<function_name>([<arguments>])
```

<p><strong>->Argumentos posicionales (obligatorios)</strong></p>
* La forma más sencilla de pasar argumentos a una función de Python es con argumentos posicionales u obligatorios.
* En la definición de la función se especifica una lista de parámetros separados por comas dentro del paréntesis:
<p><code>def productos(producto, cantidad, precio):
    print(f" {cantidad} {producto} cuestan {precio} pesos")

productos("manzanas", 5, 7.5)</code></p>

<p><em><strong>Run: </strong></em></p>
<p> 5 manzanas cuestan 7.5 pesos</p>
