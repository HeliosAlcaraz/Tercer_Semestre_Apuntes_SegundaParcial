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

#### 2.1.1.2 Definición y ventajas de su uso

* Una función es una relación o mapeo entre una o más entradas y un conjunto de salidas.
* En matemáticas, una función normalmente se representa como $$ y = f(x)$$
* *f* es una función que opera sobre la entrada *x*
* La salida de la función es *y*

<hr>

* En programación, una <em>función</em> es un bloque de código independiente para una tarea específica o un grupo de tareas relacionadas.
* Ejemplos:
  * id()
  * len()
  * max()
  * min()
<p>Ejemplo de funciones en un código:</p>  
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
