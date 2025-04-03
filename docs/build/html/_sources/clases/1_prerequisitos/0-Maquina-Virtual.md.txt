# Instalacion de Ubuntu 20.04 con VirtualBox

1.  [Descargar VirtualBox](https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html)

![Seleccion](../../_static/vm/0-VB0.jpeg)

3. Configuracion de VirtualBOX

Selecciono la opción "nueva"

![Seleccion](../../_static/vm/0-VB1.jpeg)


Coloco un nombre para la máquina virtual 

![Seleccion](../../_static/vm/0-VB2.jpeg)

Cargo la imagen ISO

![Seleccion](../../_static/vm/0-VB3.jpeg)

![Seleccion](../../_static/vm/0-VB4.jpeg)

Agrego un Usuario y contraseña para la máquina virtual

![Seleccion](../../_static/vm/0-VB5.jpeg)

Congifuro la memoria ram y el número de nucleos (se recomienda utilizar el 50% de la memoria RAM Física)

![Seleccion](../../_static/vm/0-VB6.jpeg)

Para un uso básico se recomienda un total de 30 GB de memoria

![Seleccion](../../_static/vm/0-VB7.jpeg)

Finalizo la configuración 

![Seleccion](../../_static/vm/0-VB8.jpeg)

Arrancar Máquina virtual - Al iniciar la máquina de forma automática comenzará la instalación

![Seleccion](../../_static/vm/0-VB9.jpeg)

4. Instalación de locales

Al realizarse la instalación utilizando una Máquina virtual es posible que no podamos acceder a la terminal de ubuntu, por lo cual es necesario realizar la configuración de forma manual de los *locales*

 Presionamos las teclas ctrl+alt+F3

 Ingresamos nuestras credenciales 

 Accedemos al superu suario

 ```
 su
 ```
 la contraseña es la misma que usamos para nuestro usuario regular.

 a continuación realizamos la configuración de los locales.

 ```
locale 

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  
```
y reiniciamos el sistema 
```
init 6
```
***Posibles Errores*** -

1. **Tu Usuario** no está en el archivo sudousers

**solucion**
en la terminal colocar 
```
su -
```
posteriormente agrego el nombre de usuario
```
sudo adduser [su nombre de usuario] sudo
```

2. Al momento de ejecutar la máquina virtual
NOT IN A HYPERVISOR PARTITION (HVP =0 ) [solucion](https://www.youtube.com/watch?v=XkLHhqOZmmY&t=5s)

