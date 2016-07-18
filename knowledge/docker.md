# intro
docker compose is for running multiple container s from images.
* containers communicate through ports
* local directory can be mounted into containers
 - for code
 - for configrations
 
* also we can define dependencies between containers

# container
compare to virtual machine, containers require less memory and runs faster

# services
each service is container

## parameters
* build: .
* ports
* volumes

# docker compose file reference 
https://docs.docker.com/compose/compose-file/


# docker compose file example

version: '2'
services:
  web:
    build: .
    ports:
     - "5000:5000"
    volumes:
     - .:/code
    depends_on:
     - redis
  redis:
    image: redis



# Usage
## run containers
docker-compose up 
## run one-off commands for a container
docker-compose run web env
## stop containers
docker-compose stop


