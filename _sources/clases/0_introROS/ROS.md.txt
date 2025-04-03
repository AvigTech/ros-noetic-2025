# ¿Qué es ROS?

ROS (**Robot Operating System**) es un **conjunto de herramientas, bibliotecas y convenciones** que permiten desarrollar software para robots de manera modular, escalable y reutilizable.

Aunque su nombre sugiere que es un sistema operativo, **ROS no es un sistema operativo tradicional**, sino una capa de software que corre sobre uno (normalmente Ubuntu/Linux).

---

## Ecosistema ROS

El ecosistema de ROS incluye:

- **Paquetes (packages):** Componentes de software reutilizables
- **Nodos (nodes):** Procesos que se comunican entre sí
- **Tópicos (topics):** Canales de comunicación para intercambio de mensajes
- **Servicios (services):** Comunicación síncrona entre nodos
- **Acciones (actions):** Para tareas que toman tiempo en completarse
- **Bag files:** Para grabar y reproducir datos

---

## Arquitectura de ROS

La arquitectura de ROS se basa en el modelo **peer-to-peer** y está diseñada para ser altamente distribuida. Los componentes principales son:

- `roscore`: El servidor maestro que mantiene el registro de nodos y tópicos
- `rosnode`: Herramienta de línea de comandos para interactuar con nodos
- `rostopic`: Herramienta para inspeccionar tópicos
- `rosservice`: Inspección e invocación de servicios
- `rosbag`: Grabación/reproducción de datos

---

## Plumbing vs Capabilities

- **Plumbing:** Son las herramientas base de comunicación de bajo nivel (nodos, tópicos, servicios, acciones)
- **Capabilities:** Son los sistemas de alto nivel que permiten funciones como navegación, percepción, manipulación, etc. Por ejemplo:

  - SLAM (Simultaneous Localization and Mapping)
  - Navigation Stack
  - MoveIt! para brazos robóticos
  - Percepción con cámaras y sensores

---

## Video recomendado

Para una introducción visual a ROS, puedes ver este video en YouTube:  
🔗 [¿Qué es ROS? - Introducción en español](https://www.youtube.com/watch?v=_n3wtG3n0JQ)

---

## ROS te permite

- Reutilizar código
- Integrar hardware y simuladores
- Desarrollar algoritmos de robótica avanzados
- Colaborar en proyectos a gran escala

> ROS es el corazón del software moderno para robots. Si estás empezando en robótica, dominar ROS es esencial.
