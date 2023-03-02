





UBUNTU
COMANDOS



















jan@jan:~$ sudo apt install Jan Queralt
ÍNDICE
ÍNDICE	1
CONCEPTOS GENERALES	2
SINTAXIS DE UN COMANDO	4
MOSTRAR DIRECTORIO ACTUAL	4
MOSTRAR EL CONTENIDO DE UN DIRECTORIO	4
PROPIEDADES DE LOS ARCHIVOS Y DIRECTORIOS	5
CAMBIAR DE DIRECTORIO	5
CREAR DIRECTORIO	7
BORRAR UN DIRECTORIO	8
HERRAMIENTA SUDO	9
HERRAMIENTA APT	9
CREAR MODIFICAR ARCHIVOS	10
MOSTRAR EL CONTENIDO DE UN ARCHIVO	12
BORRAR UN ARCHIVO	13
EJECUCIÓN EN FOREGROUND/BACKGROUND	14
COPIAR ARCHIVOS	14
COPIAR DIRECTORIOS	16
RENOMBRAR Y/O MOVER ARCHIVOS Y DIRECTORIOS	16
EMPAQUETAR Y COMPRIMIR	18
1a) Comprimir archivos y directorios	18
Comprimir archivos	18
Comprimir directorios	19
1b) Descomprimir archivos y directorios	20
Descomprimir archivos	20
Descomprimir directorios	20
2a) Empaquetar archivos y directorios	21
Empaquetar archivos	21
Empaquetar directorios	22
2b) Desempaquetar archivos y directorios	22
Desempaquetar archivos	22
Desempaquetar directorios	23
3a) Empaquetar y comprimir en dos pasos	23
3b) Descomprimir y desempaquetar en dos pasos	24
4a) Empaquetar y comprimir en un solo paso	24
4b) Descomprimir y desempaquetar en un paso	24
REDIRECCIONAMIENTO DE LA SALIDA ESTÁNDAR	25
TUBERÍAS	26
EJECUCIÓN SECUENCIAL DE VARIOS COMANDOS	27
PERMISOS DE ACCESO A UN ARCHIVO O DIRECTORIO	27
CREAR UN SCRIPT DE COMANDOS	27
DAR PERMISOS DE EJECUCIÓN A UN ARCHIVO (A UN SCRIPT)	30
EJECUTAR UN ARCHIVO CON PERMISOS DE EJECUCIÓN (SCRIPT)	30
CREAR UN ARCHIVO DE TEXTO CON EL COMANDO CAT	31
EJERCICIO TIPO EXAMEN	31

CONCEPTOS GENERALES

Gestor de arranque
Es un software que nos permite arrancar los diferentes sistemas operativos que tenemos instalados en la máquina (ej. GRUB, LILO).

Gestor de inicio de sesión en modo gráfico
Es una aplicación que nos permite iniciar sesión en el entorno gráfico con un usuario determinado. (EJ: LIGHTDM, GDM, KDM).

Gestor de ventanas
Es la interfaz gráfica de usuario que nos permite interactuar con el sistema operativo. (EJ: GNOME, KDE).

$
Símbolo del sistema para un usuario estándar. Un usuario estándar solamente tiene privilegios y administración (Es decir crear, modificar, eliminar archivos y directorios) dentro de su cuenta de usuario (/home/usuario).

#
Símbolo de sistema para el super usuario (root). El usuario root tiene privilegios de administración en todo el árbol de directorios del sistema operativo (es decir en todo el sistema operativo -> /). El directorio de trabajo -> /root.

Terminal
Es el intérprete de comandos (bash), permite administrar el sistema en modo comando. Siempre que abrimos un terminal nos encontramos dentro del directorio de trabajo del usuario con el que hemos iniciado sesión en el sistema operativo.

Ruta absoluta
Es el camino hacia el directorio o archivo que queremos acceder empezando desde la raíz (/). Una ruta absoluta siempre empieza con la /.

Ruta relativa
Es el camino hacia el directorio o archivo que queremos acceder empezando desde el directorio actual (Es decir des del directorio en el que me encuentro en este momento). Una ruta relativa nunca empieza con la / y siempre depende del directorio actual.


Anotación
Siempre que nos movamos por la misma rama (del árbol de directorios) donde nos encontramos en este momento, utilizaremos ruta relativa. Siempre que nos movamos por una rama diferente a la actual usaremos ruta absoluta.

Fichero o archivo
Es un objeto final(o individual) del árbol de directorios de un sistema operativo.(Ej: Archivo de texto, archivo de imagen, archivo de audio…)

Directorio o carpeta
És un contenedor de objetos del árbol de directorios de cualquier sistema operativo que puede contener archivos y/o directorios. 
.  → Equivale al directorio actual
.. → equivale al directorio anterior

/proc
Es el único directorio del sistema operativo que se carga en un disco de ram al iniciar el sistema. Contiene archivos/procesos que monitorizan el sistema.

Tab (tecla)
Sirve para autocompletar rutas, comandos y nombres de archivos.

Flechas (Arriba y abajo)
Para acceder al historial de comandos del usuario activo.

Case sensitive
Linux distingue entre mayúsculas y minúsculas, es decir en la misma ruta pueden existir varios objetos con el mismo nombre pero cuya diferencia sea alguna letra mayúscula o minúscula. EJ: Pracs, pracs, PRACS…

Salida estándar
La salida estándar es el medio por el cual un comando muestra sus resultados. Por defecto es la pantalla.

Salida estándar de error
La salida estándar de error es el medio por el cual el sistema genera mensajes de error o de advertencia a la hora de ejecutar comandos. Por defecto es la pantalla.

Entrada estándar
La entrada estándar es el medio por el cual le pasamos la información a un comando para poder ejecutarlo (opciones, argumentos, etc…). Por defecto es el teclado.

SINTAXIS DE UN COMANDO



Los corchetes ( [ ] ) marcan que lo que hay entre ellos es opcional (es decir se puede poner o no). 

Las opciones son modificadores del comando que permiten obtener más funcionalidades. 

Los argumentos indican sobre quién aplicamos el comando.



MOSTRAR DIRECTORIO ACTUAL

pwd → Muestra por pantalla el directorio en el que me encuentro en este momento(Directorio actual).


MOSTRAR EL CONTENIDO DE UN DIRECTORIO

ls → Muestra por pantalla el contenido del directorio actual
ls -l → Muestra por pantalla el contenido del directorio actual mostrando las propiedades de los archivos y directorios que contiene.

ls nom_directori → Muestra por pantalla el contenido del directorio que le pasamos como argumento al comando ls.

ls -l nom_directori → Muestra por pantalla el contenido del directorio que le pasamos como argumento al comando ls mostrando las propiedades de cada uno de los archivos y directorios que contiene.

ls -a → Muestra por pantalla el contenido del directorio actual incluyendo los archivos y directorios ocultos, es decir los que empiezan por “.”. (EJ: .bashrc).

ls -la → Muestra las propiedades del archivo(-l) y los archivos ocultos(-a).



PROPIEDADES DE LOS ARCHIVOS Y DIRECTORIOS

ls -l nom_arxiu → Muestra por pantalla las propiedades del archivo que le pasamos como argumento al comando ls.

CAMBIAR DE DIRECTORIO

cd nom_directori → Permite entrar en el directorio con el nombre que le pasamos como argumento al comando “cd”.




CREAR DIRECTORIO

mkdir nom_directori → Para crear el directorio que le pasamos como argumento al comando “mkdir”.





BORRAR UN DIRECTORIO

rm -r nom_directori → Para borrar el directorio que le pasamos como argumento al comando “rm” “-rf”.


HERRAMIENTA SUDO

sudo es una herramienta que nos permite ejecutar comandos en modo superusuario (en modo root).

sudo comando → Para ejecutar en modo root el comando que le pasamos como argumento a la herramienta “sudo”.

También nos permite iniciar sesión en modo superusuario (en modo root) sudo su → El password que nos pide el sistema es el del usuario con el que hemos ejecutado la herramienta sudo.


HERRAMIENTA APT

apt es una herramienta que nos permite instalar aplicaciones, paquetes y librerías de software.

Es necesario ser superusuario para poder utilizar esta herramienta. 

sudo apt-get update → Para actualizar la lista de paquetes a los que apt puede acceder a través de sus fuentes. 

sources.list → archive de configuración de la herramienta apt que contiene las fuentes de repositorios de software, es decir direcciones de servidores de internet de donde descargar las aplicaciones. 

sudo apt-get install nom_aplicació → Para instalar la aplicación (o paquete o librería de software) que le pasamos como argumento a la herramienta apt.

sudo apt-get remove nom_aplicació → Para desinstalar la aplicacion (o paquete o libreria de software) que le pasamos como argumento a la herramienta apt.




CREAR MODIFICAR ARCHIVOS

modo gráfico

gedit nom_archiu → Para crear o modificar el archivo que le pasamos como argumento al comando “gedit”. Si el archivo no existe se crea y si existe se entra en modo edición para poder modificar su contenido.



modo comando

vim nom_archiu → Para crear o modificar el archivo que le pasamos como argumento al comando “vim”. Si el archivo no existe se crea y si existe se entra en modo edición para poder modificar su contenido. 

i → Para entrar en modo insertar, es decir para poder modificar el nombre del archivo. 
esc → Para salir del modo insertar y de cualquier otro modo. Esto nos permitirá introducir nuevas órdenes. 
:w → Para guardar cambios 
:q → Para salir sin guardar. 
:wq → Para guardar y Salir. 
:x → Para guardar y salir. 
:q! → para forzar la salida sin guardar.






MOSTRAR EL CONTENIDO DE UN ARCHIVO
cat nom_arxiu → Muestra por pantalla el contenido del archivo que le pasamos como argumento al comando “cat”. Si el contenido del archivo es muy grande solamente se mostrará el contenido final.


more nom_arxiu → Muestra por pantalla el contenido del archivo que le pasamos como argumento al comando “more”. Si el contenido del archivo es muy grande podremos mostrar el contenido línea a línea (enter)o página a página (espacio). Presionando la tecla “q” se cancela el avance por el contenido del archi
BORRAR UN ARCHIVO
rm nom_arxiu → Para borrar el archivo que le pasamos al comando “rm” como argumento.






EJECUCIÓN EN FOREGROUND/BACKGROUND

1) Ejecución en foreground → Es la ejecución en primer plano de un comando o aplicación. Cuando lanzamos un comando o aplicación en primer plano el terminal des de donde lo hemos lanzado no nos devuelve el símbolo del sistema hasta que este comando o aplicación finaliza su ejecución, por tanto, momentáneamente no podremos lanzar más comandos o aplicaciones des de ese terminal. 

2) Ejecución en background → Es la ejecución en segundo plano de un comando o aplicación. Cuando lanzamos un comando o aplicación en segundo plano el terminal des de donde lo hemos lanzado sí nos devuelve el símbolo del sistema y por tanto nos permite lanzar otros comandos o aplicaciones aunque los anteriores no hayan finalizado.


COPIAR ARCHIVOS

1) cp nom_arxiu nom_copia → Para crear una copia de un archivo en la misma ruta donde se encuentra el archivo dándole un nombre diferente a la copia.


2) cp nom_arxiu ruta_desti → Para crear una copia de un archivo enviando la copia a una ruta diferente de la que se encuentra el archivo original, pero con el mismo nombre que el archivo original.

3) cp nom_arxiu ruta_destí/nom_copia → Para crear una copia de un archivo enviando la copia a una ruta diferente de la que se encuentra el archivo original y cambiando el nombre a la copia.


COPIAR DIRECTORIOS

1) cp -r nom_directori nom_copia →  Para crear una copia de un directorio en la misma ruta donde se encuentra el directorio dándole un nombre diferente a la copia. $ cp -r pracs pracs_c $ ls $ ls pracs_c Atención: Los ls son para comprobar que ha funcionado correctamente. 

2) cp -r nom_directori ruta_destí  →  Para crear una copia de un directorio enviando la copia a una ruta diferente de la que se encuentra el directorio original, pero con el mismo nombre que el directorio original. $ cp -r pracs pracs_c/ $ ls pracs_c/

3) cp -r nom_directori ruta_destí/nom_copia →  Para crear una copia de un directorio enviando la copia a una ruta diferente de la que se encuentra el directorio original y cambiando el nombre a la copia.


RENOMBRAR Y/O MOVER ARCHIVOS Y DIRECTORIOS

1) mv nom_arxiu nou_nom_arxiu → Para cambiar el nombre del archivo/directorio que le pasamos como argumento al comando mv.



2) mv nom_arxiu ruta_destí → Para mover el archivo/directorio que le pasamos como argumento al comando mv a una ruta diferente de la que se encuentra el archivo original.

3) mv nom_arxiu ruta_destí/nou_nom_arxiu → Para mover el archivo/directorio que le pasamos como argumento al comando mv a una ruta diferente de la que se encuentra el archivo original y con un nombre diferente.

EMPAQUETAR Y COMPRIMIR

Empaquetar consiste en juntar varios objetos del árbol de directorios del s.o. en un solo objeto.
Comprimir consiste en intentar reducir el tamaño de uno o varios objetos del árbol de directorios.


1a) Comprimir archivos y directorios

Comprimir archivos
gzip nom_arxiu1 … nom_arxiuN → Para comprimir un archivo o un conjunto de archivos. El archivo original(o archivos originales) se pierden y en su lugar se genera un archivo (o varios) con el mismo nombre que el original y con la extensión .gz.








Comprimir directorios
gzip -r nom_directori → para comprimir un directorio (o conjunto de directorios) el directorio origina(o directorios originales) no se pierde y lo que ocurre es que se comprime cada archivo del directorio(y de los subdirectorios que pueda contener) por separado, de tal forma que seguimos teniendo la misma estructura dentro del árbol de directorios. Del sistema operativo(por tanto los archivos que contiene el directorio no se empaquetan)
















1b) Descomprimir archivos y directorios

Descomprimir archivos
gzip -d pracs nom_archiu1.gz … nom_arxiuN.gz → Para descomprimir un archivo(o conjunto de archivos) el archivo comprimido(o archivos comprimidos) con la extensión .gz se pierden y en su lugar se genera el archivo original (o archivos originales) descomprimido.


Descomprimir directorios
gzip -rd nom_directori1 … nom_directoriN → Se descomprimen cada directorio por separados.






2a) Empaquetar archivos y directorios

Empaquetar archivos
tar -cfv nom_archius_empaquetats.tar nom_archiu1 nom_archiu2 … nom_archiuN -> Para empaquetar(juntar) un conjunto de archivos en un solo objeto (o en un solo archivo) con la extensión “.tar”. Los archivos originales no se pierden y a de mas se genera un archivo con la extensión “.tar” que contiene empaquetados todos los archivos que le hemos pasado al comando como argumentos.
c → Para empaquetar
v → Muestra información del proceso de emparejado
f → Forzar











Empaquetar directorios
tar -cfv nom_directori_empaquetat.tar nom_directori → Para empaquetar (juntar) un directorio en un solo objeto (o archivo) con la extensión “.tar”. El directorio original no se pierden y a de mas se genera un archivo con la extensión “.tar” que contiene empaquetados el directorio que le hemos pasado al comando como argumentos.




2b) Desempaquetar archivos y directorios

Desempaquetar archivos
tar -xvf nom_arxius_empaquetats.tar → Para desempaquetar(extraer) los archivos que se encuentran dentro del archivo “.tar” que le pasamos como argumento al comando tar con la opción -x. El archivo empaquetado(.tar) no se pierde y además obtenemos los archivos originales.
x → Desempaquetar

Desempaquetar directorios
tar -xvf nom_directori_empaquetat.tar → Para desempaquetar(extraer) el directorio empaquetado (.tar) que le pasamos como argumento al comando tar. El directorio enpaquetado(.tar) no se pierde y a demás obtenemos el directorio actual.



3a) Empaquetar y comprimir en dos pasos

1)
$ tar -cvf nom_directori_empaquetat.tar nom_directori
2)
$ gzip nom_directori_empaquetat.tar
nom_directori_empaquetat_i_comprimit.tar.gz
Después de ejecutar los dos pasos se genera el archivo(directorio) empaquetado y comprimido con la extensión “.tar.gz” . El directorio original no se pierde.





3b) Descomprimir y desempaquetar en dos pasos
1)
$ gzip -d nom_directori_empaquetat_i_comprimit.tar.gz
2)
$ tar -xvf nom_directori_empaquetat.tar
nom_directori
Después de ejecutar estos dos pasos obtenemos el directorio original. El archivo empaquetado y comprimido con la extensión “.tar.gz” se pierde

4a) Empaquetar y comprimir en un solo paso

Opción 1) 
tar -cvzf nom_directori_empaquetat_i_comprimir.tar.gz nom_directori → El directorio original no se pierde y además se genera el archivo empaquetado y comprimido con la extensión “.tar.gz”.
c → empaquetar
z → comprimir con gzip
Opción 2)
tar -cvjf nom_directori_empaquetat_i_comprimir.tar.bz2 nom_directori →El directorio original no se pierde y además se genera el archivo empaquetado y comprimido con la extensión “.tar.bz2”.
j → Comprimir con bzip2


4b) Descomprimir y desempaquetar en un paso

Opción 1)
tar -xvzf nom_directori_empaquetat_i_comprimir.tar.gz nom_directori → El archivo empaquetado y comprimido con la extensión “.tar.gz” no se pierde y además se genera el directorio original.
Opción 2)
tar -xvjf nom_directori_empaquetat_i_comprimir.tar.bz2 nom_directori → El archivo empaquetado y comprimido con la extensión “.tar.bz2” no se pierde y además se genera el directorio original.
REDIRECCIONAMIENTO DE LA SALIDA ESTÁNDAR
Redireccionar la salida estándar de un comando (que por defecto es la pantalla) nos permite enviar el resultado que genera el comando a un medio diferente como por ejemplo un archivo con la intención de que esa información sea permanente y no temporal.
Opción 1)
comando > nom_arxiu → Si el archivo no existe se crea y si existe se sobrescribe su contenido con el resultado que genera el comando.












Opción 2)
comando >> nom_arxiu → Si el archivo no existe se crea y si existe el resultado que genera el comando se añade al final de lo que contenga el archivo.

TUBERÍAS
Una tubería es una herramienta que permite que la información que genera un comando sea procesada por otro comando. 
Al comando que se encuentra a la izquierda de la tubería se le redirecciona la salida estándar, de tal forma que el resultado que genera en lugar de enviarse por la pantalla se envía a la tubería.
Al comando que se encuentra a la derecha de la tubería se le redirecciona la entrada estándar, de tal forma que lo que tiene que procesar el comando en lugar de pasárselo por teclado o recibe de la tubería (es decir, sirve para filtrar información). Se pueden enlazar tantas tuberías como sean necesarias.



EJECUCIÓN SECUENCIAL DE VARIOS COMANDOS
Opción 1)
comando1 ; comando2 ; comando 3 ; … ; comandoN → La ejecución secuencial nos permite ejecutar varios comandos en una misma línea de terminal (Uno detrás de otro). Si alguno de los comandos falla no se rompe la secuencia, es decir se ejecutarán todos los comandos que no fallen siguiendo el orden marcado por la secuencia. Esta forma de ejecución secuencial es útil cuando los comandos que ejecutamos son independientes entre si.
Opción 2)
comando1 && comando2 && comando && … && comandoN → La ejecución secuencial en modo seguro nos permite ejecutar varios comandos en una misma línea del terminal. Si alguno de los comandos falla, se rompe la secuencia, es decir solamente se ejecutan los comandos de la secuencia que estén antes del comando que haya provocado el fallo
PERMISOS DE ACCESO A UN ARCHIVO O DIRECTORIO
r -> Lectura
w -> Escritura
x -> Ejecución
(-) -> Permiso desactivado 





CREAR UN SCRIPT DE COMANDOS
Un script es un archivo ejecutable que en su interior contiene una serie de ordenes (comandos) que siguiendo una lógica determinada realizan una o varias funciones.


$ vim script1

i -> insertar




Comando1
Comando2
Comando3

esc -> salir del editor
:x guardar y salir


DAR PERMISOS DE EJECUCIÓN A UN ARCHIVO (A UN SCRIPT)
El comando para cambiar los permisos de acceso és chmod.
chmod +x nom_archiu → Para dar (añadir) permisos de ejecución a todos los usuarios (propietario, grupo propietario, resta de usuarios) de un archivo, respetando el resto de permisos tal y como están.


EJECUTAR UN ARCHIVO CON PERMISOS DE EJECUCIÓN (SCRIPT)

$ ./nom_arxiu_executable











CREAR UN ARCHIVO DE TEXTO CON EL COMANDO CAT





EJERCICIO TIPO EXAMEN

ejercicio_tipo_examen.pdf
