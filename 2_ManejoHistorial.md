# Ejercicios de manejo del historial de cambios

Para hacer estos ejercicios es necesario haber hecho antes los ejercicios de creación y actualización de repositorios

## Ejercicio 1

1. Mostrar el historial de cambios del repositorio.
2. Crear la carpeta **capitulos** y crear dentro de ella el fichero **capitulo1.txt** con el siguiente texto:

    ![Ejercicio 2.1](imagenes/ejercicio21.png)


3. Git es un sistema de control de versiones ideado por Linus Torvalds.
4. Añadir los cambios a la zona de intercambio temporal.
5. Hacer un commit de los cambios con el mensaje “Añadido capítulo 1.”
6. Volver a mostrar el historial de cambios del repositorio.

~~~
git log
git add .
git commit -m “Añadido capítulo 1.”
~~~

## Ejercicio 2

1. Crear el fichero capitulo2.txt en la carpeta capitulos con el siguiente texto.
   
    ![Ejercicio 2.1.2](imagenes/ejercicio212.png)

1. Añadir los cambios a la zona de intercambio temporal.
2. Hacer un commit de los cambios con el mensaje “Añadido capítulo 2.”
3. Mostrar las diferencias entre la última versión y dos versiones anteriores.

~~~
Author: jordi <jordisorfer1997@gmail.com>
Date:   Thu Oct 14 12:06:04 2021 +0200

    añadido capitulo 2

diff --git a/capitulos/capitulo2.txt b/capitulos/capitulo2.txt
new file mode 100644
index 0000000..9e94826
--- /dev/null
+++ b/capitulos/capitulo2.txt
@@ -0,0 +1,4 @@
+el flujo de trabajo basico con git consiste en:
+1- hacer cambios en el repositorio.
+2-Añadir los cambios a la zona de intercambio temporal
+3-hacer un commit de los cambios
\ No newline at end of file

$ git log
commit cb39005823c1efc5e828aae1ab4bc5a0efc95d45 (HEAD -> master)
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

    añadido indice del libro
~~~

## Ejercicio 3

1. Crear el fichero capitulo3.txt en la carpeta capitulos con el siguiente texto.

    ![Ejercicio 2.3.1](imagenes/ejercicio231.png)   

2. Añadir los cambios a la zona de intercambio temporal.
3. Hacer un commit de los cambios con el mensaje “Añadido capítulo 3.”
4. Mostrar las diferencias entre la primera y la última versión del repositorio.

~~~
Author: jordi <jordisorfer1997@gmail.com>
Date:   Thu Oct 14 12:15:50 2021 +0200

    añadido capitulo 3

diff --git a/capitulos/capitulo3.txt b/capitulos/capitulo3.txt
new file mode 100644
index 0000000..4f5ac1a
--- /dev/null
+++ b/capitulos/capitulo3.txt
@@ -0,0 +1 @@
+git permite la creacion de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas
\ No newline at end of file
~~~

## Ejercicio 4

1. Añadir al final del fichero indice.txt la siguiente línea:

    ![Ejercicio 2.4.1](imagenes/ejercicio241.png)

2. Añadir los cambios a la zona de intercambio temporal.
3. Hacer un commit de los cambios con el mensaje “Añadido capítulo 5 al índice.”
4. Mostrar quién ha hecho cambios sobre el fichero indice.txt.

~~~
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
~~~