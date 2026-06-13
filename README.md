<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/a/a7/React-icon.svg" width="90" alt="React">
  &nbsp;&nbsp;
  <img src="https://nodejs.org/static/images/logo.svg" width="130" alt="Node.js">
  &nbsp;&nbsp;
  <img src="https://cdn.worldvectorlogo.com/logos/prisma-2.svg" width="110" alt="Prisma">
</p>

# 🛒 E-Commerce Platform (TFG)

Aplicación web Full Stack desarrollada como **Trabajo de Final de Grado (DAW)**.  
El proyecto simula una tienda de componentes electrónicos estilo PCComponentes, permitiendo la navegación de productos, gestión de carrito, sistema de usuarios con roles y panel de administración completo.

La aplicación está construida con **React en el frontend**, **Node.js + Express en el backend**, **Prisma ORM** y **PostgreSQL en Supabase**, siguiendo una arquitectura modular y escalable.

---

## 🔗 Repositorio original para ver el proyecto

Este proyecto fue desarrollado en equipo como Trabajo de Final de Grado.

👉 https://github.com/USUARIO/REPO-ORIGINAL

---

## 🔗 Project Overview

La plataforma permite a los usuarios navegar libremente por un catálogo de productos electrónicos, visualizar detalles completos (incluyendo contenido multimedia como imágenes y vídeos) y realizar compras simuladas sin pasarela de pago real.

El sistema implementa autenticación, control de acceso por roles y rutas protegidas tanto para clientes como para administradores.

---

## 👤 User Roles

### 🧑 Cliente
- Registro e inicio de sesión
- Navegación por catálogo de productos (rutas públicas)
- Visualización de detalles de productos con contenido multimedia
- Gestión de carrito de compra
- Simulación de proceso de compra
- Historial de pedidos
- Consulta de datos personales

### 🛠️ Administrador
- Panel de administración completo
- Gestión de usuarios (visualización, modificación y eliminación)
- Gestión de pedidos
- Gestión de productos:
  - Creación de productos
  - Edición de productos
  - Desactivación de productos (no eliminación física para mantener integridad del historial)
- Supervisión general del sistema

---

## 🌐 Routing System

La aplicación se estructura en tres niveles de rutas:

### 🟢 Rutas públicas
- Página principal (Home)
- Catálogo de productos
- Detalle de producto

### 🔐 Rutas protegidas
- Requieren autenticación mediante JWT
- Verificación de sesión activa
- Acceso a carrito y acceso a perfil

### 🔴 Rutas de administrador
- Requieren autenticación + rol admin
- Acceso exclusivo al panel de gestión

---

## ⚙️ Tech Stack

### Frontend
- React
- Librerías de internacionalización (multi-idioma)
- React Router
- Gestión de estado y componentes reutilizables

### Backend
- Node.js
- Express.js
- Prisma ORM (gestión segura y tipada de base de datos)
- Arquitectura por capas:
  - Routes
  - Controllers
  - Middlewares

### Database
- PostgreSQL
- Supabase

---

## 🔐 Authentication & Security

El sistema de autenticación está basado en **JSON Web Tokens (JWT)** almacenados en **cookies HTTP-only**, lo que mejora la seguridad al evitar el acceso directo desde JavaScript del cliente.

Se han implementado medidas avanzadas de seguridad:

- Autenticación mediante JWT
- Uso de cookies HTTP-only, Secure y SameSite
- Protección frente a ataques **XSS (Cross-Site Scripting)** mediante uso de cookies HTTP-only, evitando acceso al token desde JavaScript.
- Mitigación de ataques **CSRF (Cross-Site Request Forgery)** mediante configuración de cookies (`SameSite`, `Secure`) y CORS controlado.
- Configuración controlada de **CORS**
- Middleware de verificación de tokens en backend
- Control de acceso basado en roles (User / Admin)
- Protección de rutas privadas y administrativas

---

## 🧱 Backend Architecture

El backend sigue una arquitectura estructurada y modular:

- **Routes** → Definición de endpoints
- **Controllers** → Gestión de la petición y respuesta
- **Services** → Lógica de negocio
- **Middlewares** → Autenticación y autorización
- **Prisma ORM** → Abstracción de acceso a datos, evitando queries SQL directas y reduciendo el riesgo de inyecciones SQL.

---

## 🛍️ Main Features

- Catálogo de productos estilo e-commerce real
- Visualización detallada de productos
- Sistema de carrito de compra
- Simulación de pagos
- Gestión de pedidos
- Panel de administración completo
- Control de usuarios y roles
- Arquitectura escalable y modular
- Sistema de autenticación seguro

---

## 🎓 Academic Project

Este proyecto fue desarrollado como **Trabajo de Final de Grado (DAW)**.

El objetivo principal fue simular una aplicación e-commerce real aplicando una arquitectura full stack moderna, separando claramente frontend y backend, e implementando funcionalidades avanzadas como autenticación, control de roles y gestión de datos.

Durante su desarrollo se trabajaron conceptos como:

- Arquitectura cliente-servidor
- APIs REST
- Autenticación y autorización con JWT
- Seguridad web (XSS, CSRF, CORS)
- Se utilizó Prisma ORM como capa de acceso a datos, lo que permitió trabajar con una abstracción segura sobre la base de datos, evitando queries SQL directas y reduciendo vulnerabilidades como SQL Injection.
- Gestión de bases de datos relacionales
- Desarrollo de SPA con React
- Diseño de backend escalable con Node.js
- Buenas prácticas de desarrollo profesional

---

## ⚠️ Disclaimer

Este proyecto es únicamente académico y de demostración y la funcionalidad de compra es simulada y no se procesan pagos reales.
