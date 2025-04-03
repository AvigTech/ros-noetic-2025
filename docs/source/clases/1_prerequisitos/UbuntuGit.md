# Ubuntu y GitHub

En esta sección aprenderás los fundamentos básicos de **Ubuntu** y **GitHub**, dos herramientas esenciales en el desarrollo con **ROS (Robot Operating System)**.

---

## Ubuntu

Ubuntu es un sistema operativo basado en Linux ampliamente utilizado en el desarrollo con ROS, debido a su estabilidad, soporte de comunidad y compatibilidad.

### Comandos básicos de Ubuntu (Terminal)

Aquí tienes una tabla con comandos fundamentales del sistema operativo Ubuntu:

| Categoría              | Comando                           | Descripción                          |
|------------------------|-----------------------------------|--------------------------------------|
| **Navegación**         | `ls`                              | Lista archivos del directorio actual |
|                        | `cd nombre/`                      | Cambia al directorio especificado    |
|                        | `pwd`                             | Muestra la ruta del directorio actual |
| **Archivos y carpetas**| `mkdir nueva/`                    | Crea una carpeta nueva               |
|                        | `touch archivo.txt`               | Crea un archivo vacío                |
|                        | `rm archivo.txt`                  | Elimina un archivo                   |
|                        | `rm -r carpeta/`                  | Elimina una carpeta y su contenido   |
| **Paquetes**           | `sudo apt update`                 | Actualiza el índice de paquetes      |
|                        | `sudo apt install nombre_paquete` | Instala un paquete                   |
| **Permisos**           | `chmod +x script.sh`              | Da permiso de ejecución a un script  |

---

### Permisos en directorios y archivos

En Linux, cada archivo o carpeta tiene **permisos asociados** para:

- **Usuario (u)**: el dueño del archivo
- **Grupo (g)**: usuarios del mismo grupo
- **Otros (o)**: el resto del sistema

Los permisos se definen con números:

| Número | Permiso     | Significado                |
|--------|-------------|----------------------------|
| `7`    | `rwx`       | leer, escribir, ejecutar   |
| `6`    | `rw-`       | leer y escribir            |
| `5`    | `r-x`       | leer y ejecutar            |
| `4`    | `r--`       | solo lectura               |
| `2`    | `-w-`       | solo escritura             |
| `1`    | `--x`       | solo ejecución             |
| `0`    | `---`       | sin permisos               |

---

### Ejemplo: `chmod 666 archivo.txt`

Este comando asigna permisos `rw- rw- rw-`, lo que significa:

- **Usuario** puede leer y escribir
- **Grupo** puede leer y escribir
- **Otros** pueden leer y escribir

> No es recomendable usar `chmod 666` en archivos sensibles, ya que cualquiera podría modificarlos.

Para carpetas, los permisos de ejecución (`x`) también son necesarios para poder **entrar al directorio**. Por ejemplo:

```bash
chmod 755 mi_carpeta/
```

Esto da permisos `rwx r-x r-x`, lo cual permite entrar a la carpeta y leer su contenido sin permitir modificaciones por otros.


### Claves SSH

ROS se usa frecuentemente en redes. Por eso, generar una clave SSH para GitHub es muy útil para trabajar de forma segura:

```bash
ssh-keygen -t ed25519 -C "tu_correo@ejemplo.com"
cat ~/.ssh/id_ed25519.pub
```

Agrega esa clave pública a tu cuenta de GitHub.

---

## GitHub

GitHub es una plataforma de control de versiones basada en Git que permite almacenar, compartir y colaborar en código fuente. Es ideal para proyectos ROS, especialmente al trabajar en equipos o distribuir paquetes.

### Comandos básicos de Git

```bash
# Configurar usuario
git config --global user.name "Tu Nombre"
git config --global user.email "tu_correo@example.com"

# Clonar un repositorio
git clone https://github.com/usuario/repositorio.git

# Crear y subir cambios
git add .
git commit -m "Descripción del cambio"
git push origin main

# Sincronizar cambios
git pull origin main
```

---

## Relación con ROS

- **Ubuntu** es el sistema oficial y más estable para ejecutar ROS (especialmente ROS Noetic y ROS 2 Foxy).
- **GitHub** permite almacenar paquetes ROS, compartir código con la comunidad y reutilizar módulos.
- Es común ver repositorios de GitHub con paquetes ROS que se pueden clonar y compilar directamente en `catkin_ws` o `ros2_ws`.

---

¡Dominar Ubuntu y GitHub te abrirá las puertas al desarrollo profesional en robótica con ROS!
