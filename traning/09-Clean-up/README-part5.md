## Part 5. Clean up

It's important to clean up unused stopped containers, old images, etc.

- Remove all stopped containers:

  `docker rm $(docker container ls -a -q)`
- Remove all unused images 
  `docker image prune`
  
- Remove all dangling images:

  `docker image rm $(docker images -f dangling=true)`

- Remove all unused containers, volumes, networks and dangling images (add -a to remove any unreferenced images as well):

  `docker system prune`

[Go to Useful Commands](README-commands.md)

###### Credit https://github.com/excellalabs/docker-workshop-1
