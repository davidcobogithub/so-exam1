# Primer Parcial

**Nombre:** David Felipe Cobo Plazas

**Código:** A00309844

**URL repositorio:** https://github.com/davidcobogithub/so-exam1.git 
_____

# Solución Parcial  

##  1. Descarga y validación del ISO de Debian 9
 
**1.** Descargar la imagen de [Debian 9](https://www.debian.org/).

![](ImagenesSO/descarga/c1_LI.jpg)

**2.** Una vez se ha completado la descarga de la imagen, verificamos su MD5 para ver si es la correcta. Utilizamos el programa [MD5 Checksum Utility](https://download.cnet.com/MD5-SHA-Checksum-Utility/3001-2092_4-10911445.html)

![](ImagenesSO/descarga/c2.jpg)
 
**3.** Una vez se ha completado la descarga del MD5 Checksum Utility, abrimos el programa y aparecerá como lo muestra la figura:

![](ImagenesSO/descarga/c3.jpg)

**4.** Le damos click en el botón Browse, que nos permite buscar la imagen descargada de Debian 9.

**5.** Seleccionamos la imagen y damos abrir, como lo muestra la figura:

![](ImagenesSO/descarga/c4.jpg)

**6.** Ahora vamos a ir a la siguiente URL [Debian Checksum](https://cdimage.debian.org/debian-cd/9.4.0/amd64/bt-cd/) que contiene los archivos MD5, SHA-1, SHA-256 y SHA-512 que servirán para verificar la descarga de la imagen de Debian 9.

**7.** Bajamos, buscamos y seleccionamos el archivo SHA512SUMS, como lo muestra la figura:

![](ImagenesSO/descarga/c5_LI.jpg)

**8.** Luego,copiamos el Checksum que corresponde a la imagen descargada, como se muestra en la figura:

![](ImagenesSO/descarga/c6_LI.jpg)

**9.** Pegamos en el campo de texto que dice Hash  y damos click en el botón Verify.

**10.** Si todo ha quedado bien, aparecerá un mensaje de confirmación exitoso así:

![](ImagenesSO/descarga/c8.jpg)

##  2. Instalación de Debian 9 en VirtualBox

**1.** Abrimos el programa VirtualBox.

**2.** Le damos damos click en el botón Nueva para crear una nueva maquina virtual.

**3.** En el campo de texto Nombre basta solo con escribir Debian y automáticamente el campo Tipo cambiará a Linux y el campo Versión cambiará a Debian(64-bit).

**4.** Damos click en el botón Next y configuramos el tamaño de memoria y el tipo de disco duro que desee y que sea compatible con los recursos de hardware.

**5.** Una vez ha finalizado, damos click derecho sobre la maquina virtual de Debian creada y damos click en la opción Configuración... 

**6.** En la opción Sistema, en el campo Orden de arranque arrastramos el item Disco Duro hacia arriba con el fin de dejarlo de primero en el orden de arranque.

**7.** Luego, en la opción Almacenamiento, Panel de Dispositivos de almacenamiento, nos ubicamos en el item Controlador, damos click en el ícono Agregar una unidad óptica y seleccionamos el disco verificado anteriormente.

**8.** Una vez terminamos de configurar la maquina virtual, la seleccionamos y le damos click en el botón Iniciar.

**9.** Una vez iniciada la máquina, seleccionamos Graphical Install.

**10.** Seleccionamos el idioma, la ubicación y la configuración de teclado deseada. Posteriormente, se procederá a instalar los componentes y a configurar la red.

**11.** Procedemos a la configuración de la red (nombre de la máquina y el dominio) y la configuración de usuario (contraseña de root y si queremos crear un nuevo usuario con su contraseña).

**12.** Asignamos un nombre a la máquina. Por ejemplo, Debian.

**13.** Se indica un nombre para el equipo e identificar el dominio al que quieres que pertenezca este equipo, en mi caso escribí local.

**14.** Ahora, configuramos la partición de discos: utilizamos el modo guiado, seleccionamos el disco a usar Debian9, seleccionamos la opción Todos los ficheros en una partición y finalizamos el particionado del disco confirmando los cambios.

**15.** En este paso comenzará la instalación del sistema base y luego procedemos a configurar el gestor de paquetes, seleccionando la región y el servidor ftp a utilizar, en este caso debian.uniminuto.edu.

**16.** Luego nos preguntará si deseamos analizar otro CD o DVD, aquí seleccionamos la opción NO, debido a que se hará la instalación por red.

**17.** Luego nos aparece la configuración del proxy, que en este caso lo dejamos en blanco y damos click en el botón Continuar.

**18.** También nos preguntará si deseamos participar en la encuesta sobre el uso de paquetes, aquí yo seleccioné la opción NO.

**19.** Ahora, seleccionamos los paquetes a instalar, en este caso eligiremos: GNOME, Servidor de impresión, SSH server, Utilidades estándar del sistema, Entorno de escritorio y Servidor Web. 

**20.** Comenzará la descarga e instalación de los paquetes seleccionados.

**21.** Una vez descargados los paquetes previamente seleccionados, nos pedirá instalar GRUB, que es el gestor de boot de linux. Aceptamos su instalación y seleccionamos el Disco Duro en mi caso /dev/sda.

**22.** Seguirá la instalación final del sistema y finalmente deberá aparecer un mensaje de Instalación completada, como lo muestra la figura:  

![](ImagenesSO/instalacion/c17.jpg)

**23.** Damos click en le botón Continuar y la máquina virtual se reiniciará.

**24.** Una vez reiniciada la máquina, ingresamos con nuestro usuario y password al sistema.

## Información del Sistema Operativo Debian 9.

**1.** Una vez se ha iniciado la sesión, abrimos la consola Terminal del sistema.

**2.** Para obtener la información del sistema operativo, usamos los siguientes comandos: 

cat /proc/version
Linux version 4.9.0-6-amd64 (debian-kernel@lists.debian.org) (gcc version 6.3.0 20170516 (Debian 6.3.0-18+deb9u1) ) #1 SMP Debian 4.9.82-1+deb9u3 (2018-03-02)

lsb_release -a
No LSB modules are available.
Distributor ID:	Debian
Description:	Debian GNU/Linux 9.4 (stretch)
Release:	9.4
Codename:	stretch

uname -a
Linux debian 4.9.0-6-amd64 #1 SMP Debian 4.9.82-1+deb9u3 (2018-03-02) x86_64 GNU/Linux

**3.** Adjunto imagen de comandos en Terminal:

![](ImagenesSO/instalacion/t1.jpg)

##  3. Configuración de red para la conexión a través de Putty
