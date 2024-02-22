# Servidor SAMBA en Docker
Antes de crear y levantar el contenedor, crear la carpeta a compartir y darles los permisos (777)

mkdir -p $HOME/docker/samba/compartido && \
chmod 777 -R $HOME/docker/samba/compartido

crear docker-compose.yml

levantar el contender

docker-compose up -d

Para añadir más carpetas, modificar el fichero config/smb.config dentro del contenedor. Una vez modificado, añadir las rutas en el docker-compose y levantarlo de nuevo.

docker exec -i -t CONTENEDOR /bin/bash

También se puede copiar el fichero a local desde el contenedor y modificarlo

docker cp CONTENEDOR:config/smb.conf .

Para copiarlo de nuevo al contenedor

docker cp /RUTA-FICHERO/smb.conf CONTENEDOR:config/smb.conf

![Docker-Emblem](https://github.com/JLalib/docker-samba/assets/57844755/23e20d48-41f1-4642-be8c-2008075f7f84) ![samba](https://github.com/JLalib/docker-samba/assets/57844755/b1e1f84a-d96f-4c32-981b-76a37a258435)

