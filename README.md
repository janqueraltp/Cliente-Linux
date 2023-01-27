# Cliente-Linux
## Administración de Linux en modo comando
### SIOMONO - SMIX 1

## Conceptos generales
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
