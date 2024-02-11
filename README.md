# Comandos_Docker

instalamos docker https://docs.docker.com/engine/install/ubuntu/ <br>
si hay problemas de permisos https://docs.docker.com/engine/install/linux-postinstall/ <br>
docker run hello-word <br>
docker images <br>
docker search ubuntu || docker pull ubuntu || 
docker ps (procesos en ejecución)
docker ps -a (hstorial)
eliminamos un contenedor
docker rm [NAME | COINTAINER ID]
iniciar un proceso finalizado 
docker start [NAME | CONTAINER ID]
nginx - como apache
Ejemplo de Nginx relacionado con los puertos
  docker pull nginx (instalación de la imagen)
  docker run nginx (Lo iniciamos)
  docker ps (en una nueva terminal)
  vemos el puerto interno que usa, 80/tcp
  docker stop (id) paramos el servicio
  le asignamos a ese puerto interno del docker uno externo para usar en el servidor
  docker run -p 3000:80 nginx (se inicia el servisio con el puerto vinculado)
  docker run -p 3000:80 -d nginx (detached, contenedor ejecutandose en segundo plano sin tener terminal bloqueada)


Para eliminar todos los contenedores (historial)
docker ps (procesos ejecutados)
docker ps -a (historial de procesos)
docker ps -aq (historial pero solo ids)
docker rm $(docker ps -aq) (borramos todas los procesos)
