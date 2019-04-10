# GNU/Linux

Este curso busca dar una vista general y basica del entorno linux. Este explica un poco de la historia para entender desde sus origenes que lo hace tan robusto. Ademas se explican comandos basicos de navegacion, estructura de los directorios, permisos e instalacion de paquetes usando apt.

## Historia

* GNU: Un conjunto de aplicaciones libres

* Linux: Un kernel libre

### GNU/Linux es un clon de UNIX

UNIX es un sistema operativo creado por AT&T que sigue el estandar POSIX

POSIX es un estandar de como hacer un sistema operativo. Este estandar lo maneja el IEEE.

### Linux es libre, no gratis

* La libertad de un usuario para ejecutar, copiar, distribuir, estudiar, cambiar y mejorar el software
* Linux es software libre y tiene licencia GLP
* Se puede hacer todo pero si se cambia tambien debe tener licencia GLP

### Podemos categorizar sistemas UNIX por 

* Sistemas operativos que trabajan bajo el estandar POSIX (ej. MacOSX, IOS, Android, GNU/Linux)
* Distros de Linux (ej. Ubuntu, PopOS, Manjaro, Arch)
* Ambientes de desktop (ej. KDE, GNOME, Unity)

### Filosofia

* Todo es un archivo
* Navaja suiza
* Es libre
* El poder de lo simple

## Estructura de archivos

![ups](./assets/filesystem.png "Imagen de referencia de estructura de archivos")

## Comandos basicos

* man (man comando) -> Retorna el manual de uso de un comando
* sudo (sudo comando) -> Ejecuta comando como admin
* pwd -> Muestra la ruta al directorio actual
* ls (ls directorio/que/quiero/listar)-> Muestra contenidos de un directorio
* cd (cd ruta/al/nuevo/directorio)-> Cambia de directorio al directorio destino
* mkdir (mkdir nombreDelDirectorio)-> Crea un nuevo directorio
* cp (cp archivo destino/de/copia)-> Copia un archivo de un directorio a otro
* mv (mv archivo destino/del/archivo)-> Mueve un archivo a otro directorio, tambien se puede usar para renombrar archivos
* more, less, cat (more archivo)-> Muestra contenido de un archivo
* nano (nano archivo)-> Editor de texto
* head (head archivo)-> Muestra 10 primeras lineas de un archivo
* tail (tail archivo)-> Muestra 10 ultimas lineas de un archivo
grep (grep palabra archivo)-> Busca linea por linea de un archivo si contiene la palabra
* top -> Muestra recursos del sistema
* free -> Memoria utilizada
* ps -ef -> Procesos en ejecucion
* netstat -an -> Conecciones de red
* kill (kill -9 PID) -> Mata proceso con el PID que se pasa

### Redireccion de salida estandar

* | -> Envia resultado del primer programa como entrada del segundo (ej. ls /etc | grep va, este comando lista los contenidos de la carpeta /etc y muestra solamente aquellos que contienen "va")
* ">" -> Toda salida que tenga un programa la guarda en un archivo, si ya existe ese archivo lo borra y escribe desde 0 (ej. ls /etc > lectura, Este comando guarda en un archivo que se llama "lectura" los contenidos del directorio /etc)
* ">>" -> Toda salida que tenga un programa la guarda en un archivo, si ya existe ese archivo escribe abajo de todo lo que tiene escrito (ej. ls /etc > lectura, Este comando guarda en un archivo que se llama "lectura" los contenidos del directorio /etc)

## Permisos

[Esta pagina tiene un buen tutorial de permisos](https://www.guru99.com/file-permissions.html)

## Instalar paquetes con apt

* apt-get update -> Actualiza repositorios de paquetes
* apt-get upgrade -> Actualiza todos lo paquetes instalados
* apt-get install paquete -> Instala un paquete
* dpkg --list -> Lista paquetes instalados
* apt-get --purge remove paquete -> Desinstala un paquete

## Taller
[Realice el taller propuesto para afianzar conocimientos](./LinuxTaller.pdf)