#Learning about Docker

1. Net Ninja Docker Crash Course

   - Spin Up an Node API.

   - Important Docker Commands

     - `basic commands`

       - docker system prune -a
         `all containers iamges and volumes to be deleted`

       - docker images `list all the iamges`
       - docker ps `list all running containers`
       - docker ps -a `list all containers we have`
       - docker image rm myapp `delete an image named myapp`
       - docker image rm myapp -f
         `delete an image named myapp forcefully even if it is being used`
       - docker contianer rm myapp_c myapp_c1 myapp_c2 ...
         `to delete any container`
       - docker build -t myapp:v1 .
         `to build the current file into a container, -t for a tag/name, . is the relative path to the Dockerfile, :v1 is the version`

     - `to run new container form a image`

       - docker run --name myapp_c myapp
         `naming and running blocking the terminal`
       - docker run --name myapp_c -d myapp
         `naming and running unblocking the terminal`
       - docker run --name myapp_c -p
         4000(`exposing the port in localhost`):4000(`port exposed in the docker file`)
         -d myapp
         `naming and running unblocking the terminal with port for localhost`

     - `to start and stop a container`

       - docker stop myapp_c `stop a running container`
       - docker start myapp_c `start an already existing continer`

   - Understood Layer Caching
     - can copy the package.json file first then add the RUN npm install and
       then run the COPY . . and following for better caching and faster loads.

- Container & Image Management
  - to delete an image it should'nt be in use with any container otherwise it
    will give an error
