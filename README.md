# MAIA Taller 8 - Tablero bankchurn en contenedor

Repositorio del Taller 8 (Proyecto - Desarrollo de Soluciones, MAIA Uniandes):
despliegue del tablero de bankchurn en un contenedor Docker sobre una instancia EC2.

El tablero consulta la API de prediccion de abandono, cuya ubicacion se define en
tiempo de ejecucion mediante las variables de entorno `API_URL` y `API_PORT`.

## Estructura

- `Dockerfile`: definicion de la imagen `bankchurn-dash`.
- `app/`: codigo fuente del tablero (Dash + gunicorn).

## Uso en la maquina virtual

```bash
sudo docker build -t bankchurn-dash:latest .
sudo docker run -p 8050:8050 -it -e PORT=8050 -e API_URL=X.Y.Z.W -e API_PORT=8001 bankchurn-dash
```
