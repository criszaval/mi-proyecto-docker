## 🐳 Ejecución con Docker

Este proyecto está preparado para ejecutarse en contenedores utilizando Docker con una configuración de *multi-stage build*.

### Requisitos previos
- Tener instalado [Docker](https://www.docs.docker.com/get-docker/).

### 1. Construir la imagen Docker
Ejecuta el siguiente comando en la raíz del proyecto:
```bash
docker build -t next-app-docker .