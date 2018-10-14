# WDD Docker Setup

Docker container setup for PHP development in PACE Web Development
Diploma program

## Instructions

1. Clone this repository
2. CD into cloned folder
3. Create folder `app` 
4. Create a `public` folder inside `app`, or use composer:

```bash
composer create-project \  
 package/package --prefer-dist app

```

Your folder structure should look like this:

```

this_folder
    - .docker
        Dockerfile
        vhosts.conf
    - app
        - public

```

5. Run container:

```bash
docker-compose up --build
```

## Advanced

If you like, you may edit the `Dockerfile`, `vhosts.conf` and `docker-compose.yml` file to create a custom setup

```
vi .docker/Dockerfile

vi .docker/vhosts.conf

vi docker-compose.yml

```

## Accessing the container via bash shell

1. run `docker ps` to get the names of your running containers.
2. run the following command to shell into the container:

```
docker exec -it d76d3fc85182 bash
```

## Run PHPUnit 

1. Shell into the container (see previous point)
2. Add phpunit to your `composer.json` and install
3. run PHPUnit from the `vendor/bin` folder:


```bash
vendor/bin/phpunit
```


