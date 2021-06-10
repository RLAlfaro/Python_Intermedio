### Funciones Intermedias Python

### Funciones Intermedias I

```py

```

### Funciones Intermedias II

1. Actualiza los valores en diccionarios y listas

* Cambia el valor 10 en x a 15. Una vez que haya terminado, x ahora debería ser [[5,2,3], [15,8,9]].
* Cambia el apellido del primer alumno de 'Jordan' a 'Bryant'
* En el directorio sports_directory, cambia 'Messi' a 'Andres'
* Cambia el valor 20 en z a 30
```py
x = [ [5,2,3], [10,8,9] ] 
x[1][0] = 15
print(x)

students = [
     {'first_name':  'Michael', 'last_name' : 'Jordan'},
     {'first_name' : 'John', 'last_name' : 'Rosales'}
]
students[0]['last_name'] = 'Bryantt'
print(students[0])

sports_directory = {
    'basketball' : ['Kobe', 'Jordan', 'James', 'Curry'],
    'soccer' : ['Messi', 'Ronaldo', 'Rooney']
}
sports_directory['soccer'][0] = 'Andres'
print(sports_directory['soccer'])

z = [ {'x': 10, 'y': 20} ]
z[0]['y'] = 30
print(z[0])
```

2. Itera a través de una lista de diccionarios

* Crea una función iterateDictionary(some_list)que, dada una lista de diccionarios, la función recorra cada diccionario de la lista e imprime cada clave y el valor asociado. Por ejemplo, dada la siguiente lista:

```py
## Ejercicio 2

students = [
         {'first_name':  'Michael', 'last_name' : 'Jordan'},
         {'first_name' : 'John', 'last_name' : 'Rosales'},
         {'first_name' : 'Mark', 'last_name' : 'Guillen'},
         {'first_name' : 'KB', 'last_name' : 'Tonel'}
    ]
iterateDictionary(students) 
# La salida debería ser: (Está bien si cada clave y valor quedan en dos líneas separadas)
# Bonus: Hacer que aparezcan exactamente así!
first_name - Michael, last_name - Jordan
first_name - John, last_name - Rosales
first_name - Mark, last_name - Guillen
first_name - KB, last_name - Tonel
```

```py
def iterateDictionary(lst):
    for elem in lst:
        str_elem = ''

        for llave, valor in elem.items():
            str_elem += f"{llave} - {valor}"

        print(', '.join(str_elem))

students = [
         {'first_name':  'Michael', 'last_name' : 'Jordan'},
         {'first_name' : 'John', 'last_name' : 'Rosales'},
         {'first_name' : 'Mark', 'last_name' : 'Guillen'},
         {'first_name' : 'KB', 'last_name' : 'Tonel'}
    ]
```

3. Obtén valores de una lista de diccionarios

* Crea una función iterateDictionary2(key_name, some_list)que, dada una lista de diccionarios y un nombre de clave, la función imprima el valor almacenado en esa clave para cada diccionario. Por ejemplo, iterateDictionary2 ('first_name', students) debería generar: (Michael, John, Mark, KB)

* Y iterateDictionary2('last_name', students) debería generar: (Jordan, Rosales, Guillen, Tonel)
```py
def iterateDictionary2(key_name, some_list):
    for i in range(len(some_list)):
        print(some_list[i][key_name])
iterateDictionary2 ('first_name', students)
iterateDictionary2('last_name', students)
```

```py
# Opcion 2
def iterateDictionary2(key_name, some_list):
    llaves, valores  = [], []
    for i in range(len(some_list)):
        for llave, valor in some_list[i].items():
            llaves.append(llave)
            valores.append(valor)
    for i in range(len(llaves)):
        if key_name == llaves[i]:
            print(valores[i])
```

4. Itera a través de un diccionario con valores de listas
* Crea una función printInfo(some_dict)que, dado un diccionario cuyos valores son todas listas, imprima el nombre de cada clave junto con el tamaño de su lista, y luego imprima los valores asociados dentro de la lista de cada clave. Por ejemplo: 
```py

```

```py
## Sample

dojo = {
   'locations': ['San Jose', 'Seattle', 'Dallas', 'Chicago', 'Tulsa', 'DC', 'Burbank'],
   'instructors': ['Michael', 'Amy', 'Eduardo', 'Josh', 'Graham', 'Patrick', 'Minh', 'Devon']
}
printInfo(dojo)
# output:
7 LOCATIONS
San Jose
Seattle
Dallas
Chicago
Tulsa
DC
Burbank
    
8 INSTRUCTORS
Michael
Amy
Eduardo
Josh
Graham
Patrick
Minh
Devon
```
