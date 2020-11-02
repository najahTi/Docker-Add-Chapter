# Docker-Add-Chapter

# Docker Project : 
This project create a list of chapter in a browser, using NodeJS, express and mongodb.

## Command to launch : 
* Clone the repository
* In the root do `docker-compose up`
* [localhost](http://localhost:80)

## Docker-compose :
```

version: '3'
services:
  app:
    container_name: docker-node-mongo
    restart: always
    build: .
    ports:
      - '80:3000'
    external_links:
      - mongo
  mongo:
    container_name: mongo
    image: mongo
    ports:
      - '27017:27017'
```
