# 🐳 Proyecto Next.js con Docker (Multi-Stage Build)

Este repositorio contiene una aplicación web desarrollada en **Next.js** y contenerizada utilizando **Docker** bajo estrictas buenas prácticas de infraestructura moderna, garantizando un entorno de desarrollo y producción consistente, aislado y portable.

---

## 📋 Características de la Práctica
- **Node.js 20 Alpine:** Imagen base ligera y segura optimizada para producción.
- **Multi-Stage Build (Construcción por etapas):** Separa las dependencias, la compilación y el entorno de ejecución final para reducir el tamaño de la imagen.
- **Salida Standalone:** Configuración optimizada en Next.js para empaquetar únicamente los archivos indispensables.
- **Optimización de seguridad:** Ejecución del contenedor bajo un usuario sin privilegios de root (`nextjs`).
- **Archivo `.dockerignore`:** Exclusión de archivos y carpetas innecesarias (`node_modules`, `.next`, `.git`, etc.) para acelerar el proceso de construcción.

---

## ⚙️ Requisitos Previos
Asegúrate de tener instalado en tu sistema:
- [Docker](https://docs.docker.com/get-docker/)

---

## 🚀 Instrucciones de Construcción y Ejecución

Sigue estos pasos en tu terminal para poner en marcha el proyecto localmente utilizando contenedores:

### 1. Construir la imagen de Docker
Ejecuta el siguiente comando en la raíz del proyecto para generar la imagen (asegúrate de incluir el punto `.` al final):
```bash
docker build -t next-app-docker .

docker run -p 3000:3000 --name mi-app-container next-app-docker

Abre tu navegador web de preferencia y accede a la siguiente dirección:
 http://localhost:3000
