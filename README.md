# ejercicios-de-tuplas

Qué son las tuplas En Python, una tupla es un conjunto ordenado e inmutable de elementos del mismo o diferente tipo.

Las tuplas se representan escribiendo los elementos entre paréntesis y separados por comas.

(1, "a", 3.14) (1, 'a', 3.14) En realidad no es necesario escribir los paréntesis para indicar que se trata de una tupla, basta con escribir las comas, pero Python escribe siempre los paréntesis:

1, "a", 3.14 (1, 'a', 3.14) La función len() devuelve el número de elementos de una tupla:

len((1, "a", 3.14)) 3 Una tupla puede no contener ningún elemento, es decir, ser una tupla vacía.

() () len(()) 0 Una tupla puede incluir un único elemento, pero para que Python entienda que nos estamos refiriendo a una tupla es necesario escribir al menos una coma.

El ejemplo siguiente muestra la diferencia entre escribir o no una coma. En el primer caso Python interpreta la expresión como un número y en el segundo como una tupla de un único elemento.

(3) 3 (3,) (3,) Python escribe una coma al final en las tuplas de un único elemento para indicar que se trata de un tupla, pero esa coma no indica que hay un elemento después:

(3,) (3,) len((3,)) 1

3.10. Tipo tuplas Las tuplas son objetos de tipo secuencia, específicamente es un tipo de dato lista inmutable. Esta no puede modificarse de ningún modo después de su creación.

3.10.1. Métodos Son muy similares a las listas y comparten varias de sus funciones y métodos integrados, aunque su principal diferencia es que son inmutables. El objeto de tipo tupla integra una serie de métodos integrados a continuación:

3.10.1.1. count() Este método recibe un elemento como argumento, y cuenta la cantidad de veces que aparece en la tupla.

valores = ("Python", True, "Zope", 5) print "True ->", valores.count(True) True -> 1 print "'Zope' ->", valores.count('Zope') 'Zope' -> 1 print "5 ->", valores.count(5) 5 -> 1 3.10.1.2. index() Comparte el mismo método index() del tipo lista. Este método recibe un elemento como argumento, y devuelve el índice de su primera aparición en la tupla.

valores = ("Python", True, "Zope", 5) print valores.index(True) 1 print valores.index(5) 3 El método devuelve un excepción ValueError si el elemento no se encuentra en la tupla, o en el entorno definido.

valores = ("Python", True, "Zope", 5) print valores.index(4) Traceback (most recent call last): File "", line 1, in ValueError: tuple.index(x): x not in tuple 3.10.2. Convertir a tuplas Para convertir a tipos tuplas debe usar la función tuple(), la cual está integrada en el interprete Python.

Truco Para más información consulte las funciones integradas para operaciones de secuencias.

3.10.3. Ejemplos A continuación, se presentan algunos ejemplos de su uso:

Ejemplo simple de tupla

Ejemplo de tuplas anidadas
Ejemplo de tuplas anidadas

operación asignación de valores de una tupla en variables
Operación asignar de valores de una tupla en variables

Cuidar seguimiento del número de la numeración

Una tarea común es iterar sobre una secuencia mientras cuidas el seguimiento de la numeración de un elemento.

Podría usar un bucle while con un contador o un bucle for usando la función range() y la función len():

tecnologias = ('Zope', 'Plone', 'Pyramid') for i in range(0, len(tecnologias)): ... print i, tecnologias[i] ... 0 Zope 1 Plone 2 Pyramid Pero, Python provee la palabra reservada enumerate para esto:

Caso real de conexión a BD

A continuación, un ejemplo más apegado a la realidad que busca establecer una conexión a una BD:

conexion_bd = "127.0.0.1","root","qwerty","nomina", print ("Conexión típica:", conexion_bd) print (type(conexion_bd)) conexion_completa = conexion_bd, "3307","10", print ("\nConexión con parámetros adicionales:", conexion_completa) print (type(conexion_completa))

print ("\n")

print ("IP de la BD:", conexion_completa[0][0]) print ("Usuario de la BD:", conexion_completa[0][1]) print ("Contraseña de la BD:", conexion_completa[0][2]) print ("Nombre de la BD:", conexion_completa[0][3]) print ("Puerto de conexión:", conexion_completa[1]) print ("Tiempo de espera en conexión:", conexion_completa[2])

print ("""\nMás información acerca de MySQL y Python
http://mysql-python.sf.net/MySQLdb.html\n""")

print ("\nIterar tupla con función enumerate") © 2021 GitHub, Inc. Terms Privacy Security Status Docs Contact GitHub Pricing API Training Blog About
