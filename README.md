# LeadsBridge Laravel Code Challenge
This is a standard laravel application that will be used as a code challenge for the back-end engineers.

## Getting started

### Requirements
- Docker Desktop (for Win and Mac) or Docker Compose (for Linux)

### Installation

The application will start using Laravel Sail, a built-in solution for running your Laravel project using Docker.
To get started, you only need to install [Docker Desktop](https://www.docker.com/products/docker-desktop/) (if you are using Windows or a Mac) or [Docker Compose](https://docs.docker.com/compose/install/) (if you are using Linux)

#### 

Navigate inside the project directory and execute the following command:

```shell
docker run --rm \
-u "$(id -u):$(id -g)" \
-v $(pwd):/var/www/html \
-w /var/www/html \
laravelsail/php80-composer:latest \
composer install --ignore-platform-reqs
```

This will install laravel sail and automatically execute composer install inside the container

When the process is done, execute the command:

```shell
./vendor/bin/sail up
```

_This command needs some time and pulls all the needed images._

When the process is done you will see the application running. If you navigate to http://localhost:49201 (or your port specified in APP_PORT) you should see the standard Laravel application


