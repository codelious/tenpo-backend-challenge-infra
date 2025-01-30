# 📌 **Tenpo Backend Challenge `docker-compose`**

Este repositorio corresponde al proyecto Tenpo Backend Challenge y contiene el `docker-compose.yml` para levantar toda la infraestructura localmente.

* Author: Rodrigo Espinoza Aguayo
* Email: rodrigo.espinoza.aguayo@gmail.com

---

# 🚀 Infraestructura Local con Docker Compose

Este proyecto proporciona un entorno de ejecución local utilizando **Docker Compose**, permitiendo levantar la base de datos PostgreSQL, Redis y el servicio `tenpo-backend-challenge`.

## 📦 **Servicios incluidos**
| Servicio                | Imagen utilizada |
|-------------------------|-----------------|
| **PostgreSQL**          | `postgres:15` |
| **Redis**               | `redis:7.0` |
| **Tenpo Backend Challenge** | `codelious/tenpo-backend-challenge:latest` |

---

## 🛠 **Requisitos previos**
Antes de ejecutar este entorno, asegúrate de tener instalados:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

---

## 🚀 **Cómo ejecutar el entorno local**
1. Clonar este repositorio:
   ```sh
   git clone https://github.com/codelious/tenpo-backend-challenge-infra.git
   cd tenpo-backend-challenge-infra
   ```

2. Ejecutar el siguiente comando para levantar todos los servicios:
   ```sh
   docker-compose up -d
   ```

3. Verificar que los contenedores están corriendo:
   ```sh
   docker ps
   ```

---

## 📝 **Servicios expuestos**
| Servicio               | URL/Comando de Acceso |
|------------------------|----------------------|
| **PostgreSQL**         | `localhost:5432` |
| **Redis**              | `localhost:6379` |
| **Tenpo Backend Challenge** | `http://localhost:8080` |

📌 **Notas:**
- Para conectarte a **PostgreSQL**, usa las credenciales definidas en `docker-compose.yml`:
    - **Usuario:** `user`
    - **Contraseña:** `password`
    - **Base de datos:** `calculation_db`
- **Redis** está configurado para funcionar sin autenticación.
- **Tenpo Backend Challenge** es el microservicio principal que gestiona cálculos con porcentaje dinámico. 
  - Puedes encontrar el código fuente en el siguiente repositorio: 👉 [Repositorio en GitHub: `tenpo-backend-challenge`](https://github.com/codelious/tenpo-backend-challenge)

---

## 🛑 **Cómo detener los servicios**
Para detener y eliminar los contenedores, ejecuta:
```sh
  docker-compose down
```

Si deseas eliminar volúmenes y caché:
```sh
  docker-compose down -v
```
