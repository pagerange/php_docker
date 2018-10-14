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

docker_setup
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
