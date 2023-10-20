#Learning about Docker

1. Net Ninja Docker Crash Course

   - Spin Up an Node API.

   - Important Docker Commands

     - `basic commands`

       - docker images `list all the iamges`
       - docker ps `list all running containers`
       - docker build -t myapp . `to build the current file into a container`

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
