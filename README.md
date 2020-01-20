# hooper

Lets see what 5 hours can do...


**Source:** https://blog.usejournal.com/scraping-50-million-tweets-for-5-in-5-hours-9dca3031a734


# Installation

For local dev:

 - On Mac: https://treehouse.github.io/installation-guides/mac/mongo-mac.html
 - On Ubuntu: https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-18-04
 
With docker, `docker-compose.yml`:

```
version: '3.1'
services:
  mongodb:
    image: mongo:4.0.0-xenial
    volumes:
      - './mongodb:/data/db'
    networks:
      - backend
    deploy:
      placement:
        constraints: [node.role == manager]
    environment:
      MONGO_INITDB_ROOT_USERNAME: <username>
      MONGO_INITDB_ROOT_PASSWORD: <password>
    ports:
      - "27017:27017"
networks:
  backend:
    external: true
```
 
