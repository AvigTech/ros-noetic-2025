# 📝 Guía de Estructura Markdown para Documentación ROS

Este documento sirve como referencia básica de los elementos comunes en Markdown que puedes usar en la documentación del curso ROS Noetic SMR.

---

## 📚 Índices y Subíndices

### 🧩 Subtítulo de tercer nivel

Puedes estructurar tus secciones así:

```text
# Título principal
## Subtítulo
### Sub-subtítulo
```

---

## ✍️ Formatos de texto

- **Negrita**: `**negrita**` → **negrita**
- *Cursiva*: `*cursiva*` → *cursiva*
- `Código en línea`: usa comillas invertidas `` `comando` `` → `comando`

---

## ✅ Listas

### Lista con viñetas

- Item 1
- Item 2
  - Subitem 2.1
  - Subitem 2.2

### Lista numerada

1. Paso uno
2. Paso dos
3. Paso tres

---

## 💻 Bloques de código

```bash
roscore
rosrun turtlesim turtlesim_node
```

:: 
  dddd

```python
def saludo():
    print("Hola ROS")
```

---

## 🖼️ Imágenes

Puedes mostrar imágenes locales o externas:

```text
![Descripción de la imagen](../_static/ejemplo.png)
```

Ejemplo:

![Robot](https://upload.wikimedia.org/wikipedia/commons/3/3a/Robot_Pepper.jpg)

---

## 🔗 Enlaces

- [Sitio oficial de ROS](https://www.ros.org/)
- [Repositorio del curso](https://github.com/AvigTech/ros-noetic-smr)

---

## 📦 Estructura de carpetas

```text
ros-noetic-smr/
├── docs/
│   ├── index.md
│   └── clases/
│       └── clase1.md
├── .github/
└── README.md
```

---

## 🧠 Notas y advertencias

```{note}
Este es un mensaje informativo tipo "note".
```

```{warning}
Este bloque es una advertencia. Úsalo para precauciones o errores comunes.
```
