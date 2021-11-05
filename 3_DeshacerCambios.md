# Ejercicios de deshacer cambios

Para hacer estos ejercicios es necesario haber hecho antes los ejercicios sobre historial de cambios

## Ejercicio 1

1. Eliminar la última línea del fichero **indice.txt** y guardarlo.
2. Comprobar el estado del repositorio.
3. Deshacer los cambios realizados en el fichero **indice.txt** para volver a la versión anterior del fichero.
4. Volver a comprobar el estado del repositorio.

~~~git
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.txt

no changes added to commit (use "git add" and/or "git commit -a")
~~~
~~~~
On branch master
nothing to commit, working tree clean
~~~~

## Ejercicio 2

1. Eliminar la última línea del fichero **indice.txt** y guardarlo.
2. Añadir los cambios a la zona de intercambio temporal.
3. Comprobar de nuevo el estado del repositorio.
4. Quitar los cambios de la zona de intercambio temporal, pero mantenerlos en el directorio de trabajo.
5. Comprobar de nuevo el estado del repositorio.
6. Deshacer los cambios realizados en el fichero **indice.txt** para volver a la versión anterior del fichero.
7. Volver a comprobar el estado del repositorio.

~~~git
solución
~~~

## Ejercicio 3

1. Eliminar la última línea del fichero **indice.txt** y guardarlo.
2. Eliminar el fichero **capitulos/capitulo3.txt**.
3. Añadir un fichero nuevo **capitulos/capitulo4.txt** vacío.
4. Añadir los cambios a la zona de intercambio temporal.
5. Comprobar de nuevo el estado del repositorio.
6. Quitar los cambios de la zona de intercambio temporal, pero mantenerlos en el directorio de trabajo.
7. Comprobar de nuevo el estado del repositorio.
8. Deshacer los cambios realizados para volver a la versión del repositorio.
9. Volver a comprobar el estado del repositorio.

~~~~
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    capitulos/capitulo3.txt
        new file:   capitulos/capitulo4.txt
        modified:   index.txt
~~~~
~~~~
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    capitulos/capitulo3.txt
        modified:   index.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        capitulos/capitulo4.txt

no changes added to commit (use "git add" and/or "git commit -a")
~~~~
~~~~
On branch master
nothing to commit, working tree clean
~~~~
## Ejercicio 4

1. Eliminar la última línea del fichero **indice.txt** y guardarlo. 
2. Eliminar el fichero **capitulos/capitulo3.txt**.
3. Añadir los cambios a la zona de intercambio temporal y hacer un commit con el mensaje “Borrado accidental.” 
4. Comprobar el historial del repositorio. 
5. Deshacer el último commit pero mantener los cambios anteriores en el directorio de trabajo y la zona de intercambio temporal. 
6. Comprobar el historial y el estado del repositorio. 
7. Volver a hacer el commit con el mismo mensaje de antes. 
8. Deshacer el último commit y los cambios anteriores del directorio de trabajo volviendo a la versión anterior del repositorio.
9. Comprobar de nuevo el historial y el estado del repositorio.

~~~~
commit 28aed81a49bf8d98313e44d132a86d48cd06f806 (HEAD -> master)
Author: jordi <jordisorfer1997@gmail.com>
Date:   Wed Oct 20 06:37:24 2021 +0200

    borrado accidental

commit 5c143ba0640424bce8cc37b829e3e9f22657823d
Author: jordi <jordisorfer1997@gmail.com>
Date:   Tue Oct 19 08:47:02 2021 +0200

    Añadido capitulo 5 al indice

commit 16144d21b2c7d4bcdda61be484b047b2c64be781
Author: jordi <jordisorfer1997@gmail.com>
Date:   Thu Oct 14 12:15:50 2021 +0200

    añadido capitulo 3

commit cb39005823c1efc5e828aae1ab4bc5a0efc95d45
Author: jordi <jordisorfer1997@gmail.com>
Date:   Thu Oct 14 12:06:04 2021 +0200

    añadido capitulo 2
    commit e7cd8b5ad5652ea5d16ea35f003c0dd4f58dcd8d
Author: jordi <jordisorfer1997@gmail.com>
Date:   Wed Oct 13 09:39:00 2021 +0200

    añadido capitulo 1

commit 928312ba831429b3a413cd3e6941372d8c737117
Author: jordi <jordisorfer1997@gmail.com>
Date:   Wed Oct 13 09:05:11 2021 +0200

    capitulo3 sobre gesion de ramas al indice

commit 54616472b590166b529b0b187c2df3b666a173c2
Author: jordi <jordisorfer1997@gmail.com>
Date:   Wed Oct 13 08:56:54 2021 +0200

~~~~
~~~~
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    capitulos/capitulo3.txt
        modified:   index.txt
~~~~
~~~~
$ git reset --hard head~1
HEAD is now at 5c143ba Añadido capitulo 5 al indice
~~~~
~~~~
commit 5c143ba0640424bce8cc37b829e3e9f22657823d (HEAD -> master)
Author: jordi <jordisorfer1997@gmail.com>
Date:   Tue Oct 19 08:47:02 2021 +0200

    Añadido capitulo 5 al indice

diff --git a/index.txt b/index.txt
index 442f9b8..6ce7d4f 100644
--- a/index.txt
+++ b/index.txt
@@ -1,4 +1,5 @@
 Capitulo 1: introduccion a git
 Capitulo 2: Flujo de trabajo basico
 Capitulo 3: Gestion de ramas
-Capitulo 4: Repositorios
\ No newline at end of file
+Capitulo 4: Repositorios
+Capitulo 5: Conceptos avanzados
\ No newline at end of file
~~~~