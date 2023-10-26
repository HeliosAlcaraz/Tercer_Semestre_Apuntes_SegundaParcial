# APUNTES DE LA SEGUNDA PARCIAL
## Programación Funcional 
<p><em><strong>Stringdocs:</strong></em> </p>    
<p><em><strong>REPL:</strong></em> Repeat Evual Print Loop. </p>    
<p><em><strong>Lambda:</strong></em> </p>  
<p><em><strong>Args y Kwargs:</strong></em> Pueden ser puras (tiene argumentos, entre otras cosas) e impuras (no tiene argumentos, entre otras cosas).</p>  
<p><em><strong>Args:</strong></em> Cuando se quiere que una función acepte un número arbitrario de argumentos, se usan los "args".
Los *args son un parámetro que se define como cualquier otro, pero con un asterisco delante del nombre. Python interpretará esto 
como el nombre de una tupla en la que se almacenarán todos los argumentos que se reciben.</p> 
<p><em><code>def imprime_lista(nombre_lista, *cosas):
    print("Lista de " + nombre_lista)
    for cosa in cosas:
        print(cosa)

imprime_lista("Piezas","tornillo","cable","clavo","tuerca")</code></em></p>
<hr>
<hr>
