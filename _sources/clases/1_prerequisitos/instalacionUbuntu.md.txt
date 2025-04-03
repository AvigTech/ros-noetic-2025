# Instalación de Ubuntu para usar ROS Noetic

Para el funcionamiento de ROS es necesario instalar Ubuntu.  
En este curso trabajaremos con **Ubuntu 20.04** y **ROS Noetic**.

---

## Recursos de descarga

- **Imagen ISO Ubuntu 20.04.6:**  
  [Descargar desde releases.ubuntu.com](https://releases.ubuntu.com/focal/)

---

## Opciones de instalación

### Comparativa: Partición del Disco vs Máquina Virtual

| Característica                     | Instalar en Disco (Dual Boot)                          | Máquina Virtual                            |
|-----------------------------------|--------------------------------------------------------|--------------------------------------------|
| 🔧 Rendimiento                    | Alto, accede directamente al hardware                  | Medio, depende del host y configuración    |
| 💾 Espacio dedicado               | Necesita particionar el disco real                    | Usa archivo virtual, configurable          |
| 🧰 Acceso a periféricos           | Total (puertos, GPU, cámara, etc.)                     | Limitado (USB y sensores configurables)    |
| 📦 Instalación de drivers         | Manual, igual que en una instalación real              | Generalmente menos problema con drivers    |
| 🔄 Cambiar entre SO               | Reinicio necesario                                     | Cambio instantáneo dentro del host         |
| 📚 Ideal para                     | Uso profesional, proyectos con hardware real           | Pruebas, simulación, desarrollo portable    |

---

## Tutoriales recomendados

- **Opción 1: Partición de disco (Dual Boot):**  
Es necesario utilizar la ISO descargada de Ubuntu 20.04 LTS

[Ver en YouTube](https://www.youtube.com/watch?v=_d6oT7rEoGc)

- **Opción 2: Máquina Virtual:**  
  [Guía práctica aquí](./0-Maquina-Virtual.md)

---

## Verificación de instalación de Python

Una vez dentro de Ubuntu, abre una terminal y ejecuta:

```bash
python3 --version
```

Debe mostrarse algo como `Python 3.8.x`, que es la versión por defecto en Ubuntu 20.04.
