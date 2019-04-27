# Docker Commands Quick Reference

1. Start new container

    `docker container run --publish <port>:<port> <image_name>`
    
    **Example:**
       
     To start a new nginx container on port 80,
         
        docker container run --publish 80:80 nginx
        
2. Start new container in detached mode

    `docker container run --publish <port>:<port> --detach <image_name>`

3. List currently running containers

    `docker container ls`
    
    > `docker container ps` also emits the same output. This was the old syntax.
    
4. Stop Docker container

    `docker container stop <container id>`
    
    > We don't have to type the complete container id. Usually the first 3-4 digits would be good enough to uniquely identify the container that we wish to stop out of all the currently running ones.
