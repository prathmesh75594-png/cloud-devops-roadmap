# Docker Day 2

## Topics Learned
- Pulled Ubuntu image
- Started an Ubuntu container
- Entered the container using interactive mode
- Created a file inside the container
- Understood the difference between starting a new container and restarting an existing one

## Commands Practiced

docker pull ubuntu

docker run -it ubuntu

docker ps

docker ps -a

docker start <container_id>

docker exec -it <container_id> bash

exit

## Key Learning

Images are templates.

Containers are running instances of images.

Data created inside a stopped container remains available when the same container is started again.
