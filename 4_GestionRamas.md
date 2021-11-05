# Ejercicios de gestión de ramas
## Ejercicio 1
1. Crear una nueva rama bibliografia y mostrar las ramas del repositorio.

~~~~
$ git log --graph --oneline
* 5c143ba (HEAD -> master, bibliografia) Añadido capitulo 5 al indice
* 16144d2 añadido capitulo 3
* cb39005 añadido capitulo 2
* e7cd8b5 añadido capitulo 1
* 928312b capitulo3 sobre gesion de ramas al indice
* 5461647 añadido indice del libro
~~~~

## Ejercicio 2
1. Crear el fichero capitulos/capitulo4.txt y añadir el texto siguiente
2. Añadir los cambios a la zona de intercambio temporal.
3. Hacer un commit con el mensaje “Añadido capítulo 4.”
4. Mostrar la historia del repositorio incluyendo todas las ramas

~~~~
* 794d0b1 (HEAD -> master) Añadido capitulo 4
* 5c143ba (bibliografia) Añadido capitulo 5 al indice
* 16144d2 añadido capitulo 3
* cb39005 añadido capitulo 2
* e7cd8b5 añadido capitulo 1
* 928312b capitulo3 sobre gesion de ramas al indice
* 5461647 añadido indice del libro
~~~~

## Ejercicio 3
1. Cambiar a la rama bibliografia.
2. Crear el fichero bibliografia.txt y añadir la siguiente referencia
3. Añadir los cambios a la zona de intercambio temporal.
4. Hacer un commit con el mensaje “Añadida primera referencia bibliográfica.”
5. Mostrar la historia del repositorio incluyendo todas las ramas.

~~~~
* 1762e43 (HEAD -> bibliografia) Añadida primera referencia bibliografica
| * 794d0b1 (master) Añadido capitulo 4
|/
* 5c143ba Añadido capitulo 5 al indice
* 16144d2 añadido capitulo 3
* cb39005 añadido capitulo 2
* e7cd8b5 añadido capitulo 1
* 928312b capitulo3 sobre gesion de ramas al indice
* 5461647 añadido indice del libro
~~~~

## Ejercicio 4
1. Fusionar la rama bibliografia con la rama master.
2. Mostrar la historia del repositorio incluyendo todas las ramas.
3. Eliminar la rama bibliografia.
4. Mostrar de nuevo la historia del repositorio incluyendo todas las ramas.

~~~~

*   49272d0 (HEAD -> master) Juntadas ramas
|\
| * 3e31110 Añadida primera referencia bibliografica
* | 0adf519 Añadido capitulo 4
|/
* 5c143ba Añadido capitulo 5 al indice
* 16144d2 añadido capitulo 3
* cb39005 añadido capitulo 2
* e7cd8b5 añadido capitulo 1
* 928312b capitulo3 sobre gesion de ramas al indice
* 5461647 añadido indice del libro

~~~~
## Ejercicio 5
1. Crear la rama bibliografia.
2. Cambiar a la rama bibliografia.
3. Cambiar el fichero bibliografia.txt para que contenga las siguientes referencias
4. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el
mensaje “Añadida nueva referencia bibliográfica.”
5. Cambiar a la rama master.
6. Cambiar el fichero bibliografia.txt para que contenga las siguientes referencias:
7. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el
mensaje “Añadida nueva referencia bibliográfica.”
8. Fusionar la rama bibliografia con la rama master.
9. Resolver el conflicto dejando el fichero bibliografia.txt con las referencias:
10. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el
mensaje “Resuelto conflicto de bibliografía.”
11. Mostrar la historia del repositorio incluyendo todas las ramas.

~~~~
$ git log --graph --oneline --all
*   c7593e3 (HEAD -> master) solucionando comflicto bibliografia
|\
| * 0d70141 (bibliografia) Añadido nueva referencia bibliografica
* | 8789bb9 Añadida nueva referencia bibliografica
|/
*   49272d0 Juntadas ramas
|\
| * 3e31110 Añadida primera referencia bibliografica
* | 0adf519 Añadido capitulo 4
|/
* 5c143ba Añadido capitulo 5 al indice
* 16144d2 añadido capitulo 3
* cb39005 añadido capitulo 2
* e7cd8b5 añadido capitulo 1
* 928312b capitulo3 sobre gesion de ramas al indice
* 5461647 añadido indice del libro
~~~~
