<p align="center">
  <a href="https://moodle.org/" target="blank"><img src="https://moodle.org/theme/moodleorg/pix/moodle_logo_TM.svg" width="300" alt="Moodle Logo" /></a>
</p>

# Moodle con Docker Compose

<div align="center">

[![Moodle](https://img.shields.io/badge/Moodle-4.3.3-orange?style=flat-square&logo=moodle)](https://moodle.org/)
[![Docker](https://img.shields.io/badge/Docker-Container-blue?style=flat-square&logo=docker)](https://www.docker.com/)
[![MariaDB](https://img.shields.io/badge/MariaDB-Database-003545?style=flat-square&logo=mariadb)](https://mariadb.org/)
[![phpMyAdmin](https://img.shields.io/badge/phpMyAdmin-Admin-6c7cc4?style=flat-square&logo=phpmyadmin)](https://www.phpmyadmin.net/)

</div>

Este repositorio permite desplegar un entorno completo de desarrollo para el LMS **Moodle** utilizando contenedores, facilitando la configuración de la base de datos y herramientas de gestión en cuestión de segundos.

> [!NOTE]
> **Notas de Stack:**
>
> - **Moodle v4.3.3:** Versión estable configurada para rendimiento local.
> - **MariaDB:** Utilizada como motor de base de datos relacional robusto.
> - **phpMyAdmin:** Interfaz gráfica incluida para gestionar la base de datos sin comandos SQL complejos.
> - **Aislamiento:** Todo el entorno corre bajo una red aislada de Docker para evitar conflictos de puertos en tu host.

---

> [!IMPORTANT]
> **Requisitos Previos**
>
> Es necesario tener instalados **Docker** y **Docker Compose** en tu sistema antes de proceder con el despliegue.
>
> [Documentación oficial de Docker](https://docs.docker.com/get-docker/)

---

## Configuración y Ejecución Local

### 1. Clonar el Repositorio

```bash
git clone https://github.com/froddo-dev/docker-moodle-dev.git
cd docker-moodle-dev
```

### 2. Iniciar Servicios

```bash
docker-compose up -d
```

---

## Credenciales y Acceso

| Servicio                | URL                                            | Usuario | Contraseña  |
| :---------------------- | :--------------------------------------------- | :------ | :---------- |
| **Moodle (Plataforma)** | [http://localhost:8080](http://localhost:8080) | `admin` | `passw0rd!` |
| **phpMyAdmin (DB)**     | [http://localhost:8081](http://localhost:8081) | `root`  | `moodle`    |

---

## Comandos de Utilidad

| Tarea                    | Comando                  |
| :----------------------- | :----------------------- |
| **Iniciar contenedores** | `docker-compose up -d`   |
| **Detener contenedores** | `docker-compose down`    |
| **Ver estado actual**    | `docker-compose ps`      |
| **Monitorear logs**      | `docker-compose logs -f` |
| **Reiniciar entorno**    | `docker-compose restart` |

---

## Documentación de Referencia

- [Manual de Usuario Moodle](./docs/moodle-manual.md) (si aplica)
- [Guía de Docker Compose](https://docs.docker.com/compose/)
- [Configuración MariaDB](https://mariadb.com/kb/en/documentation/)

---

## Notas de Configuración

Para personalizar el entorno, puedes editar el archivo `docker-compose.yml`.

> [!TIP]
> **Personalización:**
> Puedes cambiar los puertos de salida (ej. `8080` por `9000`) o las credenciales de la base de datos modificando las variables de entorno dentro del archivo compose.

---

> [!NOTE]
> **Nota del Desarrollador:**
> Este entorno está diseñado para facilitar el desarrollo y pruebas de plugins o temas en Moodle.

---

## Licencia

Este proyecto está bajo la [Licencia MIT](LICENSE).
