# Ejercicios de creación y actualización de repositorios

## Ejercicio 1

1. Crear un repositorio nuevo con el nombre libro y mostrar su contenido.

~~~
git init "libro"
~~~

2. Configurar Git definiendo el nombre del usuario, el correo electrónico y activar el coloreado de la salida. Mostrar la configuración final.

~~~~
git config --list

diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.name=jordi
user.email=jordisorfer1997@gmail.com
color.ui=auto
~~~~


## Ejercicio 2

1. Comprobar el estado del repositorio.
2. Crear un fichero indice.txt con el siguiente contenido:
   
    ![ejercicio1.2](imagenes/ejercicio12.png)

1. Comprobar de nuevo el estado del repositorio.
2. Añadir el fichero a la zona de intercambio temporal.
3. Volver a comprobar una vez más el estado del repositorio.

~~~
git status
*crear archivo*
git status
git add .
git status
~~~

## Ejercicio 3

Realizar un commit de los últimos cambios con el mensaje “Añadido índice del libro.” y ver el estado del repositorio.

~~~
git commit -m "añadido indice del libro"
git status
~~~

## Ejercicio 4

1. Cambiar el fichero indice.txt para que contenga lo siguiente:

    ![ejercicio1.2](imagenes/ejercicio14.png)

 
2. Mostrar los cambios con respecto a la última versión guardada en el repositorio.
3. Hacer un commit de los cambios con el mensaje “Añadido capítulo 3 sobre gestión de ramas”.

~~~
*modificar fichero*
git status
git add .
git commit -m "añadido capitulo 3 sobre gestion de ramas
~~~

## Ejercicio 5

1. Mostrar los cambios de la última versión del repositorio con respecto a la anterior.
2. Cambiar el mensaje del último commit por “Añadido capítulo 3 sobre gestión de ramas al índice.”
3. Volver a mostrar los últimos cambios del repositorio.

~~~
git show
git add .
git commit -m “Añadido capítulo 3 sobre gestión de ramas al índice.”
~~~


## Ejercicio 6

Indica a Git que quieres que ignore todos los ficheros que empiecen per “dam”, todos los que 
tengan la extensión out y las imágenes (jpg, png, bmp y gif). 

~~~
Crear fichero .gitignore 
introducir todo lo que quiera excluir
~~~

