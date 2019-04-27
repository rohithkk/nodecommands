# Docker Commands Quick Reference

1. List currently running containers

    `docker container ls`
    
    
    > `docker container ps` also emits the same output. This was the old syntax.
    
    
2. Start new container

    `docker container run --publish <port>:<port> <image_name>`
    
    **Example:**
       
     To start a new nginx container on port 80,
         
        docker container run --publish 80:80 nginx
        
3. Start new container in detached mode

    `docker container run --publish <port>:<port> --detach <image_name>`
