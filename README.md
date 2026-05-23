# Innovatech Chile

Aplicación full stack contenerizada basada en una arquitectura multicapa desplegada sobre AWS EC2 utilizando Docker y Docker Compose.

El proyecto demuestra una implementación simple de prácticas DevOps modernas integrando:

* Frontend desacoplado
* Backend REST API
* Base de datos MySQL
* Contenedores Docker
* Automatización CI/CD con GitHub Actions
* Despliegue en instancia EC2 mediante IP pública

---

# 📌 Arquitectura del Proyecto

```text
                ┌──────────────────────┐
                │      Usuario         │
                └──────────┬───────────┘
                           │
                    HTTP Requests
                           │
                ┌──────────▼───────────┐
                │      Frontend        │
                │     Dockerized       │
                │      Port 8080       │
                └──────────┬───────────┘
                           │ API Calls
                ┌──────────▼───────────┐
                │       Backend        │
                │      Node.js API     │
                │      Port 3001       │
                └──────────┬───────────┘
                           │
                     MySQL Queries
                           │
                ┌──────────▼───────────┐
                │      MySQL DB        │
                │    Internal Access   │
                │      Port 3306       │
                └──────────────────────┘
```

---

# ⚙️ Tecnologías Utilizadas

## Backend

* Node.js
* Express.js
* MySQL

## Frontend

* HTML5
* CSS3
* JavaScript Vanilla

## DevOps & Infraestructura

* Docker
* Docker Compose
* GitHub Actions
* Amazon EC2
* Linux Ubuntu Server

---

# 📂 Estructura del Repositorio

```bash
.
├── backend/
├── frontend/
├── db/
├── .github/workflows/
├── docker-compose.yml
└── README.md
```

| Carpeta              | Descripción                                     |
| -------------------- | ----------------------------------------------- |
| `frontend/`          | Interfaz gráfica de usuario                     |
| `backend/`           | API REST y lógica de negocio                    |
| `db/`                | Configuración e inicialización de base de datos |
| `.github/workflows/` | Automatización CI/CD                            |
| `docker-compose.yml` | Orquestación completa de servicios              |

---

# 🚀 Despliegue del Proyecto

## 1️⃣ Clonar repositorio

```bash
git clone https://github.com/vicenteavilac/tienda-perritos-devops.git
cd tienda-perritos-devops
```

---

## 2️⃣ Ejecutar servicios con Docker Compose

```bash
docker compose up -d --build
```

---

## 3️⃣ Acceder a la aplicación

### Frontend

```text
http://IP_PUBLICA_EC2:8080
```

### Backend API

```text
http://IP_PUBLICA_EC2:3001
```

---

# 🐳 Contenedores Docker

El proyecto está completamente contenerizado.

Cada servicio se ejecuta de manera independiente:

| Servicio | Puerto | Función               |
| -------- | ------ | --------------------- |
| Frontend | 8080   | Interfaz cliente      |
| Backend  | 3001   | API REST              |
| MySQL    | 3306   | Persistencia de datos |

La base de datos se encuentra aislada dentro de la red interna de Docker y no está expuesta públicamente.

---

# ☁️ Infraestructura AWS

El despliegue fue realizado sobre una instancia Amazon EC2 utilizando Ubuntu Server.

## Componentes principales

* EC2 Ubuntu Instance
* Docker Engine
* Docker Compose
* Security Groups
* Acceso mediante IP pública

---

# 🔄 Pipeline CI/CD

El proyecto incorpora automatización mediante GitHub Actions.

## Flujo automatizado

```text
Developer Push → GitHub → GitHub Actions → Build Docker → Deploy EC2
```

### Objetivos del pipeline

* Automatizar despliegues
* Reducir errores manuales
* Validar builds automáticamente
* Facilitar integración continua

---

# 🔐 Seguridad

Buenas prácticas implementadas:

* Separación de capas
* Contenedores aislados
* Base de datos no expuesta públicamente
* Comunicación interna mediante red Docker
* Variables de entorno desacopladas

---

# 📸 Vista General

## Servicios activos

```bash
docker ps
```

## Logs

```bash
docker compose logs -f
```

---

# 🛠️ Mejoras Futuras

* Implementación HTTPS con Nginx
* Reverse Proxy
* Terraform para infraestructura como código
* Kubernetes deployment
* Monitoring con Prometheus y Grafana
* Pipeline avanzado multi-stage
* Registro privado de imágenes Docker

---

# 👨‍💻 Autor

## Vicente Ávila

Proyecto académico/práctico orientado a implementación DevOps y despliegue cloud.

GitHub:

[vicenteavilac GitHub Profile](https://github.com/vicenteavilac?utm_source=chatgpt.com)

Repositorio:

[tienda-perritos-devops](https://github.com/vicenteavilac/tienda-perritos-devops?utm_source=chatgpt.com)

---

# ⭐ Objetivo del Proyecto

Este proyecto busca demostrar conocimientos fundamentales de:

* Arquitectura multicapa
* Contenerización
* Integración continua
* Despliegue continuo
* Cloud Computing
* Automatización DevOps
* Infraestructura moderna basada en contenedores
