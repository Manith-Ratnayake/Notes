docker images

docker pull <image_name>:<tag>

docker run

docker rmi <image_name>:<tag>

docker build -t <image_name>:<tag> .

docker ps

docker ps -a

docker run -d <image_name>

docker stop <container_id>

docker rm <container_id>

docker network ls

docker network create <network_name>

docker network connect <network_name> <container_id>

docker volume ls

docker volume create <volume_name>

docker run -v <volume_name>:<container_path> <image_name>

docker logs <container_id>

docker stats

docker-compose up

docker-compose down

docker-compose build
