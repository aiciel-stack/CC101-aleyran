# Docker Compose Guide: Nextcloud + MariaDB

## The docker-compose.yml File
```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the services: block do?
The `services:` block defines each container that makes up the application. Here it defines two services, `database` and `app`, telling Docker Compose which images to use, what environment variables to pass in, and what ports to expose for each one, so the whole stack can be started together.

## How did the Nextcloud app container know how to find the database container?
The `app` service's `MYSQL_HOST=database` environment variable tells Nextcloud to connect to a host named `database`. Docker Compose automatically creates a shared network for all services in the file and lets each service reach the others by its service name, so `database` resolves to the MariaDB container without needing its IP address.

## What is the difference between docker run and docker-compose up -d?
`docker run` starts one container at a time from a single command, which means a multi-container application has to be deployed and connected manually, one container at a time. `docker-compose up -d` reads a YAML file that defines every container, its configuration, and the network connecting them, and starts the whole stack with a single command. This makes Compose better suited for multi-tier applications, while `docker run` is suited for quick, single-container tasks like the Nginx deployment in Mission 4.
