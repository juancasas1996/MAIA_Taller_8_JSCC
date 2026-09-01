# MAIA Taller 8 - API bankchurn en contenedor

Repositorio del Taller 8 (Proyecto - Desarrollo de Soluciones, MAIA Uniandes):
despliegue de la API de bankchurn en un contenedor Docker sobre una instancia EC2.

## Estructura

- `Dockerfile`: definicion de la imagen `bankchurn-api`.
- `bankchurn-api/`: codigo fuente de la API (FastAPI + uvicorn) y el paquete del modelo.

## Uso en la maquina virtual

```bash
sudo docker build -t bankchurn-api:latest .
sudo docker run -p 8001:8001 -it -e PORT=8001 bankchurn-api
```
