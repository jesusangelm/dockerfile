# Imagen Docker con Ubuntu 14.04 LTS.

NOTA: Esta imagen docker es puramente **Experimental**

Este Dockerfile crea una imagen docker con Ubuntu 14.04 LTS la cual
se le eactualiza el repositorio y se instalan los paquetes que requieran
actualizacion. 

Tambien contiene un script extraido de el dockerfile
[Tutum-Ubuntu](https://github.com/tutumcloud/tutum-ubuntu) el cual configura
Open-SSH server y crea una clave para el usuario ROOT el cual puede obtenerse
ejecutando `docker logs <ID del contenedor>` una vez se haya creado un
contenedor a partir de esta imagen.

Para crear una imagen de este contenedor y poder conectarte a el via SSH se
debe ejecutar con el `flag` `-d` `-P` el cual indica que se ejecutara el 
contenedor en el fondo (daemonizado) y mapeando cualquier puerto expuesto en 
el contenedor hacia el exterior (host).

Se puede conectar via SSH a este contenedor con el comando:
`$ ssh -p <puerto> root@<ip>`

