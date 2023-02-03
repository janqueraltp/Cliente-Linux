# Cliente-Linux ![logoubuntu](img/log.png)
## Administración de Linux en modo comando
#### Redes locales - SMIX - [@janqueraltp](https://github.com/janqueraltp).

**Índice**
1. :page_facing_up: [Conceptos generales](#id1)
2. :books: [Sintaxis de un comando](#id2)

<div id='id1' />

## Conceptos generales :page_facing_up:
•	**Gestor de arranque** es un software que nos permite arrancar los diferentes sistemas operativos que tenemos instalados en la máquina (ej. GRUB, LILO).  
•	**Gestor de inicio de sesión en modo gráfico** es una aplicación que nos permite iniciar sesión en el entorno gráfico con un usuario determinado (ej. LIGHTDM, GDM, KDM).  
•	**Gestor de ventanas** es la interfaz gráfica de usuario que nos permite interactuar con el sistema operativo (ej. GNOME, KDE).  
•	**$** símbolo del sistema para un usuario estándar. Un usuario estándar solamente tiene privilegios de administración (es decir puede crear, modificar, eliminar archivos y directorios) dentro de su cuenta de usuario (es decir en su directorio de trabajo /home/nombre del usuario).  
•	**#** símbolo del sistema para el super usuario (root), tiene privilegios de administración en todo el árbol de directorios del sistema operativo (es decir en todo el sistema operativo (SO)  /). El directorio de trabajo del usuario root es /root.  
•	**Terminal** es el interprete de comandos (bash). Permite administrar el sistema en modo comando.
Siempre que abrimos un terminal, nos encontramos dentro del directorio de trabajo del usuario con el que hemos iniciado sesión en el sistema operativo (SO).  
•	**Ruta absoluta** es el camino hacia el directorio o archivo que queremos acceder empezando desde la raíz ( / ). Una ruta absoluta siempre empieza con la /. (ej. /home/admin/pracs/pt1).  
•	**Ruta relativa** es el camino hacia el directorio o archivo que queremos acceder empezando desde el directorio actual (es decir desde el directorio donde me encuentro en este momento).  
Una ruta relativa nunca empieza con la ( / ) y siempre depende del directorio
Actual (ej. PRACS / PT1 ).  
•	**Anotación** siempre que nos movamos por la misma rama (árbol del directorio)
donde nos encontramos en estos momentos utilizaremos una ruta relativa.
Y siempre nos moveremos por una rama diferente a la actual usaremos ruta
absoluta. 

<div id='id2' />

## Sintaxis de un comando :books:
```$comando [-opciones] [argumentos]```


•	Los corchetes ( [ ] ) marcan que lo que hay entre ellos es opcional (es decir se puede poner o no).  
•	Las opciones son modificadores del comando que permiten obtener más funcionalidades.  
•	Los argumentos indican sobre quién aplicamos el comando.  





### CREAR DIRECTORIOS
#### Mkdir nom directori :arrow_right: crear un direcrtorio   
![image](https://user-images.githubusercontent.com/116662838/215170004-9d04c9ff-b779-4f47-a3dc-4f1e4e6e6768.png)  

#### Ls :arrow_right: Mostrar directorios :arrow_right: Para comprobar que se ha creado bien  
![image](https://user-images.githubusercontent.com/116662838/215168936-bc808dad-415b-4d56-bf1d-3d0ce5b66c71.png)  

### ELIMINAR DIRECTORIO
RM -RF NOM_DIRECTORI :arrow_right: Para borrar el directorio.
### HERRAMIENTA APT
APT es una herramienta que nos permite instalar aplicaciones, paquetes y librerias de software.  
Es necesario ser superusuario para poder utilizar esta herramienta.  
Apt-get update --> Para actualizer la lista de paquetes a los que apt puede acceder atraves de sus fuentes
Sources.list --> Archivo de configuración del comando apt que contiene las fuentes de repositorio de software, direcciones de servidores de internet de donde descargar aplicaciones (fuentes).
Apt-get install nom_aplicació  Para instalar la aplicación (o paquete o librería de software)
Que le pasamos como arguemento a la herramienta APT.
Sudo apt-get install xxx  Instalar
Sudo apt-get remove xxx  Desinstalar
### HERRAMIENTAS SUDO
Es una herramienta que nos permite ejecutar comandos de modo superusuario (root)
Sudo comando  Para ejecutar en modo root el comando que le pasamos como argumento la herramienta sudo
Sudo nos permite iniciar sesión en modo superusuario  sudo su.
El password que nos solicita el sistema es el del usuario con el que hemos ejecutado al herramienta sudo

### CREAR / MODIFICAR ARCHIVOS
Gedit nom_directorio  Para crear o modificar el archivo que le pasamos como argumento al comando gedit. Si el archivo no existe se crea y si existe se entra en modo edición.

**VIM  Editor
Tecla i  insertar
Esc  para salir del modo insertar i de otros modos. Esto nos permitirá introducir nuevas ordenes.
W  Para guardar canvios
Q  Para salir sin guardar
WQ  Guardar i salir
X  Guardar i salir también
Q!  Forzar la salida sin guardar**


MOSTRAR EL CONTENIDO DE UN ARCHICVO
Cat nomarxiu  Muestra por pantalla el contenido del archivo que le pasamos por pantalla del archivo qure le pasamos como argumento al comando cat. Si el archivo es muy grande solamente se mostrara la parte final

more --> Muestra por pantalla el contenido del archivo que le pasamos por pantalla del archivo qure le pasamos como argumento al comando cat. Si el archivo es muy grande podremos mostrar el contenido linia a linia (con la tecla enter o pagina a pagina con la tecla espacio).
Presionando la tecla q se cancela el avanze por el archivo
Tabulador  Sirve para aurocompletar rutas, comandos y archivos


Las fletchas arriba y abajo sirven para mostrar el historial de comandos
Las fletxas izquierda i derecha nos sirven para movernos dentro de una linia del historial

Foreground y background
FOREGROUND
Cuando lanzamos (ejecutamos) un comando o aplicacion en primer o segundo plano, el terminal desde donde lo hemos lanzado (ejecutado) no nos devuelve el símbolo del sistema hasta que este comando o aplicación no finaliza su ejecución por tanto momentáneamente no podremos lanzar mas comandos o aplicaciones desde ese terminal
BACKGROUND
Es la ejecución en segundo plano de un comando o aplicación. Cuando lanzamos un comando o aplicación en segundo plano el terminal desde donde lo hemos lanzado sí nos devuelve el símbolo del sistema y por tanto nos permite lanzar otros comandos o aplicaciones aunque las anteriores no hayan finalizado.


COPIAR ARCHIVOS

CP  COPIAR
Para crear una copia de un archivo en la misma ruta donde se encuentra el archivo, pero dándole un nombre diferente a la copia.
Cp nom_archiu ruta_desti/nomcopia

COPIAR DIRECTORIOS
Cp (opción) nom directori ruta desti
Cp -r pracs pracs_c
Ls
Ls pracs_c

RENOVAR Y/O MOVER ARCHIVOS Y DIRECTORIOS
Mv nom-arxiu nou-nom-arxiu
Para canviar el nombre del archivo (o directorio) que le pasamos como argumento al comando mv
Para mover el archivo (o directorio) al comando mv a una ruta diferente de la que se encuentra el archivo original.

Mover y renombrar
Mr nom-arxiu ruta-desti/nou-nom-arxiu
Para mover el archive que le pasamos como arguemtno al comando mv a una ruta diferente de la que se encuentra el archivo original y con un nombre diferente



# EMPAQUETAR Y COMPRIMIR
***Empaquetar*** --> Es juntar varios objetos del arbol de directoreios del Sistema opaerativo (SO) en un solo objeto.  
***Comprimir*** -->  Consiste en intentar reducir el tamaño de uno o varios objetos del arbol de directorios del Sistema Operativo (SO). La idea   

### 1a. Comprimir archivos 📁
```gzip nombre-archivo1... nombre-archivoN```
Para comprimir un archivo o un conjunto de archivos. El archivo orgiginal (o originales) se pierden (desaparecen) y en su lugar se genera uno (o varios) archivos con el mismo nombre que el original y con la extension ```.gz```  
![image](https://user-images.githubusercontent.com/116662838/216680592-7e296ceb-dd12-4acc-99de-3d147a3cfa5a.png)  

```gzip -r nom-directori```
Para comprimir un directorio (o conjunto de directorios). El directorio original (o directorios originales) no se pierde y lo que ocurre es que se comproime cada archivo del directorio (y de los subdirectorios que pueda contener) por separado, de tal forma que seguimos teniendo la misma estructura  dentro del arbol de directorios del sistema operativo (por tanto los objetos que contiene el directorio no se empaquetan)
