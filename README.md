Docker

Para correr el container de React en interactivo:
docker run -it -p 3000:3000 CONTAINER_ID

Si agregamos -v $(pwd):/app para indicar que el directorio actual es el volumen designado para estar dentro de /app, detectará los cambios dentro de esta carpeta en tiempo real.

PAra no mapear node_modules:
docker run -it -p 3000:3000 -v $(pwd):/app -v /app/node_modules IMAGE_ID

If Reat exits with status 0:
*  web:
*     stdin_open: true
In the docker-compose.yml
docker-compose down && docker-compose up --build

Si queremos usar un container que ya corre para ejecutar otro comando:
docker exec -it CONTAINER_ID yarn test




