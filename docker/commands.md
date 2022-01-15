# Commands

| Commands | Description |
| -------- | -------- |
| `docker run -it IMAGE` | Run docker container in interactive mode to connect to it |
| `docker image` | Shows the list of pulled images | 
| `docker rmi IMAGE` | Remove image. Need to remove [container](https://stackoverflow.com/questions/51188657/image-is-being-used-by-stopped-container/51189547) as well |
| `docker ps` | Shows all running containers |
| `docker kill CONTAINER` | Stops the container from running |
| `docker system df -v` | Display amount of disk space used by docker daemon (images, containers, volumes, etc) |
| `docker system prune` | Removes unused containers, images, networks and volumes. Use `-a` to remove all. |
| `docker run -it --rm IMAGE` | Run docker container. When finished, it will remove the container |
| `docker run -dit IMAGE` | Run docker container. `-d` means the container runs detached in the background |
| `docker inspect IMAGE` | Shows info about an image |
| `docker info` | Displays host OS info |
| `docker search IMAGE` | Search for images on docker hub |
