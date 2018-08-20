# Curso-de-Administraci-n-de-Servidores-Linux
Curso de Administración de Servidores Linux


## Configuración y guía básica usando Virtualbox

* ifconfig: Permite ver las network interfaces

* ifdown [network interface]: Desactiva dicha interface

* ifup [network interface]: Activa dicha interface Los binarios se encuentran en: /sbin/if…

* ping [ip address]: Permite realizar ping a dicha IP

* ssh [ip address] o ssh [username]@[ip address]: Permite conectarse por medio de SSH a un servidor (ubicado en dicha IP)

* ssh-keygen -t rsa -b 4096 -C [your_email@example.com]: Permite generar una llave ssh tipo rsa

* ssh-copy-id -i [ssh-key address].pub [username]@[ip address]: Envia una copia de la llave ssh “pública” a un servidor (ubicado en dicha IP)
En el servidor se crea una carpeta en el home (.ssh/authorized_keys); donde almacena la llave ssh “pública”.

* sudo vim /etc/ssh/sshd_config: En este archivo de configuración se debe editar la opción para que la única forma de conectarse al servidor sea por medio de ssh y no por medio de username y password.
La opción a editar es: PasswordAuthentication [no], colocar no; para evitar la autenticación por medio de username y password

* sudo /etc/init.d/ssh restart: Reinicia el servicio ssh; y aplica los cambios

## Ayuda en línea de Aptitude

* "q": Salir.

* "?": Mostrar esta pantalla.

* "f": Borrar la lista de paquetes «nuevos».

* Arriba o "k": Mover arriba la marca de selección.

* Abajo o "j": Mover abajo la marca de selección.

* Pag Arriba o Control-b: Mover la selección hacia arriba una pantalla.

* Pag Abajo o Control-f: Mover la selección hacia abajo una pantalla.

* Inicio o Control-a: Mueve la seleccion al primer paquete de la lista.

* Fin o control-e: Mueve la selección al último paquete de la lista.

* "^": Mover la selección al padre del elemento actual.

* Enter: Expandir o contraer un grupo de paquetes.

* "[": Expandir un grupo de paquetes y todos sus subgrupos.

* "]": Contraer un grupo de paquetes y todos sus subgrupos.

* Control-t: Activa o desactiva el menú.

* "F6": Mueve a la siguiente pestaña en la vista principal.

* "F7": Mueve a la pestaña anterior en la vista principal.

* Enter: Ver información de un paquete.

* "C": Ver el registro de cambios de un paquete.

* "+": Instalar o actualizar un paquete, o eliminar su estado de bloqueo.

* "-": Eliminar un paquete.

* "=": Bloquear un paquete en su versión actual para evitar actualizaciones.

* ":": Mantener un paquete en su versión actual. A diferencia de el bloqueo, no previene futuras actualizaciones.

* "_": Eliminar un paquete con todos sus conf-files (N.T.ficheros de configuración).

* "L": Solicitar la reinstalación de un paquete.

* "M": Marcar un paquete como si hubiese sido instalado automáticamente. Los paquetes instalados automáticamente se eliminan si no los necesita ningún paquete instalado manualmente.

* "m": Marcar un paquete como instalado manualmente.

* "F": Prohibir que un paquete se actualice a una versión específica. Las versiones posteriores se instalarán automáticamente.

* "u": Actualizar la lista de paquetes disponibles.

* "U": Marcar todos los paquetes actualizables para actualizar.

* "g": Realizar todas las instalaciones, desinstalaciones y actualizaciones pendientes.

* Control-u: Deshacer la última acción o conjunto de acciones.

* "/": Realizar una búsqueda. (Por el nombre del paquete de forma predeterminada, lea el README/Manual de usuario para más información).

* "\": Realizar una búsqueda hacia atrás.

* "n": Repetir la última búsqueda.

* "N": Repetir la última búsqueda, pero en la dirección opuesta.

* "b": Buscar el siguiente paquete roto.

* "v": Mostrar todas las versiones disponibles de un paquete.

* "d": Mostrar las dependencias de un paquete.

* "r": Mostrar los paquetes que dependen de un paquete determinado.

* "D": Mostrar u ocultar el área de información de los paquetes.

* "a": Desplazar hacia arriba el área de infomación de los paquetes.

* "z": Desplazar hacia abajo el área de información de los paquetes.

* "i": Mostrar de forma sucesiva las distintas vistas de información de los paquetes.

* ",": Ver la solución de la dependencia anterior…

* ".": Vea la siguiente solución de la dependencia, generando una nueva solución si es necesario

* "<": Ver la primera solución de la dependencia.

* ">": Ver la última solución de la dependencia. En una resolución de conflicto interactiva:

* "a": Apruebe una acción, haciendo que siempre se elija sobre las alternativas, o cancele una
 aprobación.

*"r": Rechazar una acción, haciendo que nunca sea elegida, o cancelar un rechazo.

## Arquitectura
Una de las cosas más importantes que debemos entender es la estructura de archivos, el directorio raíz es /

###Directorios importantes

* /home, se almacenan los archivos de cada usuario.
* /lib, almacenas las librerías del sistema.
* /mnt, cuando montamos en el sistema dispositivos, los podemos ver en esta carpeta.
* /opt, almacenas los programas instalados de terceros.
* /root, almacena los archivos del super usuario Root.
* /sbin, archivos binarios del administrador.
* /usr, programas instalados por defecto.
* /var, se utiliza para guardar archivos de logs, backups, servidor web.
* /etc, archivos de configuración del sistema.
* /boot, guarda los archivos del arranque del sistema.
