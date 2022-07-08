# nginx-proxy

#1 Create a directory and in this directory we create a file >>> "nginx.conf"

#2 Create a "Dockerfile" that have some content, that given below:
        
FROM nginx:alpine
COPY nginx.conf /etc/nginx/nginx.conf
RUN apk update && apk add bash
CMD ["bash"]
   
   This docker file create a nginx-proxy image 
   
#     $ docker build -t reverseproxy .
      build an  image by using dockerfile and then run,
      
      $ docker run -t -i reverseproxy /bin/bash

# After this creating a docker-compose.yml to start multicontainer application by using recently created image
   
   $ docker-compose up -d
   $ docker-compose stop
   
   Using these commands to start and stop docker compose.
