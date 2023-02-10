# docker-samba
docker-compose Servidor Samba
Antes de crear y levantar el contenedor, crear la carpeta a compartir y darles los permisos (777)

mkdir -p $HOME/docker/samba/compartido && \
chmod 777 -R $HOME/docker/samba/compartido

crear docker-compose.yml

levantar el contendero

docker-compose up -d
