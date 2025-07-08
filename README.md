# gestion-tareas
Proyecto para la gestión de tareas por usuario
# 🗂️ Sistema de Gestión de Tareas – Fullstack con Microservicios y Angular

Este proyecto es una solución completa para la gestión de tareas, construida con microservicios en Node.js, frontend en Angular 19 y base de datos PostgreSQL, todo orquestado con Docker Compose.

---

## 📁 Estructura del Proyecto

Este repositorio principal contiene referencias a los siguientes submódulos:

```
gestion-tareas/
├── docker-compose.yml                      # Orquestación de servicios
├── base-datos-gestion-tareas/              # Script SQL para inicializar la base de datos
├── microservicio-autenticacion/           # Servicio de autenticación de usuarios
├── microservicio-gestion-tareas/          # Servicio de gestión de tareas
└── gestion-tareas-frontend/               # Aplicación frontend Angular 19
```

---

## 🚀 Requisitos

- [Docker](https://www.docker.com/) instalado
- [Git](https://git-scm.com/) instalado

---

## 📦 Clonar el proyecto (con submódulos)

Clona este repositorio **junto con los submódulos** necesarios:

```bash
git clone --recurse-submodules https://github.com/fsalazar89/gestion-tareas.git
cd gestion-tareas
```

> Si ya lo clonaste sin `--recurse-submodules`, puedes traer los submódulos luego con:
>
> ```bash
> git submodule update --init --recursive
> ```

---

## 🛠️ Ejecutar el sistema

Desde la raíz del proyecto, levanta todos los servicios con:

```bash
docker-compose up --build
```

Esto:
- Inicia PostgreSQL y ejecuta el script de base de datos automáticamente.
- Construye y ejecuta los microservicios de autenticación y tareas.
- Compila el frontend Angular y lo sirve mediante Nginx.

---

## 🌐 Acceso a la aplicación

Una vez todo esté corriendo, abre tu navegador y accede a:

```
http://localhost:4200
```

---

## 🧪 Endpoints principales

Estos endpoints son accedidos internamente por el frontend, pero puedes probarlos también desde Postman si lo deseas:

- Microservicio de autenticación: `http://localhost:8099/api/auth/...`
- Microservicio de gestión de tareas: `http://localhost:8098/api/tareas/...`

---

## ⚙️ Puertos utilizados

| Servicio                  | Puerto Host |
|---------------------------|-------------|
| Angular (Frontend)        | `4200`      |
| Microservicio Tareas      | `8098`      |
| Microservicio Auth        | `8099`      |
| PostgreSQL                | `5577`      |

Asegúrate de que esos puertos estén libres.

---

## 🧰 Tecnologías utilizadas

- **Angular 19** – Frontend SPA moderno
- **Node.js + Express** – Backend en microservicios
- **PostgreSQL 16** – Base de datos relacional
- **Docker y Docker Compose** – Contenedores
- **Nginx** – Servidor estático para Angular

---

## 👨‍💻 Autor

**Fernando Salazar**  
[GitHub: @fsalazar89](https://github.com/fsalazar89)

---

## 📝 Notas adicionales

- El proyecto está diseñado para ser ejecutado localmente en cualquier entorno con Docker.
- No es necesario configurar rutas ni variables de entorno manualmente.
- Para detener los servicios, puedes usar:
  ```bash
  docker-compose down
  ```
