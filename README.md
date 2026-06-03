# Sistema de Gestión Financiera Estudiantil - Backend
# AhorraPlusIA

Backend desarrollado con Spring Boot para la gestión financiera estudiantil. Proporciona una API REST segura que permite administrar usuarios, ingresos, gastos, metas de ahorro, reportes financieros y recomendaciones inteligentes mediante integración con servicios externos de Inteligencia Artificial.

## Descripción

Este proyecto implementa la lógica de negocio del sistema, la gestión de datos, la autenticación de usuarios y la comunicación con servicios externos. Está diseñado siguiendo una arquitectura por capas basada en principios SOLID para garantizar escalabilidad, mantenibilidad y seguridad.

## Características Principales

### Autenticación y Seguridad

* Registro de usuarios.
* Inicio de sesión mediante JWT.
* Recuperación de contraseña.
* Verificación de correo electrónico.
* Control de acceso basado en roles.
* Protección de endpoints mediante Spring Security.

### Gestión Financiera

* Registro de ingresos.
* Registro de gastos.
* Edición y eliminación de movimientos.
* Clasificación por categorías.
* Cálculo automático de balances.

### Metas de Ahorro

* Creación de metas financieras.
* Seguimiento automático del progreso.
* Actualización basada en movimientos registrados.

### Reportes

* Generación de estadísticas financieras.
* Consultas resumidas por períodos.
* Exportación de información.

### Inteligencia Artificial

* Integración con API externa.
* Análisis financiero automatizado.
* Recomendaciones personalizadas.

### Soporte

* Creación de tickets.
* Seguimiento de incidencias.
* Gestión administrativa.

## Arquitectura

```text
Controller
    ↓
Service
    ↓
Repository
    ↓
PostgreSQL
```

## Tecnologías Utilizadas

### Backend

* Java 17
* Spring Boot 3
* Spring Security
* Spring Data JPA
* Hibernate
* JWT
* Maven
* Lombok
* PostgreSQL

### Infraestructura

* Docker
* Docker Compose

## Estructura del Proyecto

```text
src/main/java
├── controller
├── service
├── service/impl
├── repository
├── dto
├── mapper
├── domain
├── security
└── config
```

## Endpoints Principales

### Autenticación

```http
POST /auth/register
POST /auth/login
POST /auth/forgot-password
POST /auth/reset-password
```

### Ingresos

```http
GET    /ingresos
POST   /ingresos
PUT    /ingresos/{id}
DELETE /ingresos/{id}
```

### Gastos

```http
GET    /gastos
POST   /gastos
PUT    /gastos/{id}
DELETE /gastos/{id}
```

### Metas de Ahorro

```http
GET    /metas-ahorros
POST   /metas-ahorros
PUT    /metas-ahorros/{id}
DELETE /metas-ahorros/{id}
```

### Reportes

```http
GET /reportes
```

### Recomendaciones

```http
GET  /recomendaciones
POST /recomendaciones
```

## Seguridad

* JWT Authentication.
* BCrypt Password Encoder.
* Roles y permisos.
* Validaciones backend.
* Protección de rutas privadas.
* Uso de variables de entorno para credenciales sensibles.

## Ejecución Local

```bash
mvn clean install
mvn spring-boot:run
```

## Docker

```bash
docker-compose up -d
```

## Repositorio Frontend

El frontend del proyecto se encuentra en:

https://github.com/jefersonfloz/AhorraPlusIAFrontend

