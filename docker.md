# Docker Commands Quick Reference

### Common Syntax for running Docker commands

   `docker < command > <sub command> [options ]`


1. Get the Docker Client and Server version

    `docker version`
    
2. Start new container

    `docker container run --publish <port>:<port> <image_name>`
    
    **Example:**
       
     To start a new nginx container on port 80,
         
        docker container run --publish 80:80 nginx
        
3. Start new container in detached mode

    `docker container run --publish <port>:<port> --detach <image_name>`

4. Start an existing stopped container

   `docker container start `

5. List currently running containers

    `docker container ls`
    
    > `docker container ps` also emits the same output. This was the old syntax.
    
6. Stop Docker container

    `docker container stop <container id>`
    
    > We don't have to type the complete container id. Usually the first 3-4 digits would be good enough to uniquely identify the container that we wish to stop out of all the currently running ones.
    
7. To remove all stopped containers, dangling images, unused networks,

   `docker system prune`
    
   `docker system prune -f` or `docker system prune --force` to skip the warning.
   
8. View logs from a container

    `docker container logs [options] <container id>`
    
    > Options:  -f                      follow the log output, 
    >            --tail < number >         show the last <number> lines from the logs
    
