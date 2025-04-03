# Elemento básicos de ROS

## Espacio de trabajo

En ROS (Robot Operating System), el **espacio de trabajo** (workspace) es una estructura de directorios donde se desarrolla, organiza y compila todo el código relacionado con ROS. Es una parte esencial para estructurar los paquetes, nodos y configuraciones que usarás en tus aplicaciones robóticas.

**Creación del Espacio de Trabajo**

```bash
mkdir [Nombre_del_espacio_de_trabajo]
cd [Nombre_del_espacio_de_trabajo]
mkdir src
```

El comando `mkdir` crea una nueva carpeta. `src` es la subcarpeta donde se almacenan los paquetes de ROS.

**Compilación del Workspace**

```bash
catkin_make
```

Este comando genera los directorios `build/` y `devel/`, necesarios para compilar y ejecutar los paquetes.

**Configurar entorno con .bashrc**

```bash
echo "source ~/[Nombre_del_espacio_de_trabajo]/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

Esto asegura que ROS reconozca tu espacio de trabajo cada vez que abras una terminal.

---

## Paquetes en ROS

Un **paquete** en ROS es la unidad mínima de software que contiene nodos, lanzadores, bibliotecas, archivos de configuración y dependencias.

**Crear un paquete**

```bash
cd src
catkin_create_pkg [Nombre_del_paquete] [dependencias]
```

**Dependencias comunes**

| Dependencia       | Descripción |
|-------------------|-------------|
| `roscpp`          | Librería C++ de ROS |
| `rospy`           | Librería Python de ROS |
| `std_msgs`        | Tipos de mensajes estándar |
| `sensor_msgs`     | Datos de sensores (cámaras, lidar, etc.) |
| `geometry_msgs`   | Posición, orientación, transformaciones |
| `visualization_msgs` | Visualización en RViz |
| `tf`              | Gestión de transformaciones de coordenadas |
| `rviz`            | Herramienta 3D de visualización de datos robóticos |

**Compilar el paquete**

```bash
cd ..
catkin_make
```

---

## Ejercicio

A continuación creamos un espacio de trabajo denominado `catkin_ws` y el primer paquete a crear será `pkg_smr`

```bash
mkdir catkin_ws
cd catkin_ws
mkdir src
```
Compilación:


```bash
catkin_make
```

Configuración del entorno

```bash
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

---

## Creación de Nodos en ROS

Un **nodo** es una unidad ejecutable dentro del sistema distribuido de ROS. Se comunica mediante tópicos, servicios o acciones.

**Crear nodo Python**

```bash
cd src/[Nombre_del_paquete]/src
gedit [Nombre_del_archivo.py]
chmod +x [Nombre_del_archivo.py]
```

**Estructura básica del nodo - usando `while not rospy.is_shutdown()`**

```python
#!/usr/bin/env python3

import rospy

def main():
    rospy.init_node('primer_nodo', anonymous=True)
    rate = rospy.Rate(1)  # 1 Hz
    while not rospy.is_shutdown():
        rospy.loginfo("Mi primer nodo en ROS - while not rospy.is_shutdown()")
        rate.sleep()

if __name__ == '__main__':
    try:
        main()
    except rospy.ROSInterruptException:
        pass
```

**Estructura con `rospy.spin()`**

```python
#!/usr/bin/env python3

import rospy

def timer_callback(event):
    rospy.loginfo("Mi primer nodo en ROS - rospy.spin()")

def main():
    rospy.init_node('segundo_nodo', anonymous=True)
    rospy.Timer(rospy.Duration(1), timer_callback)
    rospy.spin()

if __name__ == '__main__':
    try:
        main()
    except rospy.ROSInterruptException:
        pass
```

---

Con esto, tienes la base sólida para crear, compilar y ejecutar nodos en ROS.