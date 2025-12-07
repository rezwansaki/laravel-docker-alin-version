# Laravel-Docker-Alin-Version

Laravel-Docker-Alin-Version is a pre-built and customizable Docker environment for Laravel. With this setup, you can quickly create and manage Laravel projects inside Docker without complex configurations.

This project was originally customized by Masum, and later further adapted and refined by me to match my own development needs.

## Last Modifed Date

07-December-2025 by Alin

## Check 'default.conf' file

open the default.conf file: <br>
'Laravel-Docker-Alin-Version/nginx/default.conf' <br>

Change these information (if need): <br>
server_name 192.168.1.177; <br>
listen 80;

## Run this command in the terminal for making structure

docker compose run --rm project composer global require laravel/installer

## Run this command in the terminal to Create a Laravel project in 'src' folder

laravel new src

## Modify '.env' file from 'src' folder according to docker-compose.yml

```
APP_URL=https://localhost
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=testdb
DB_USERNAME=alin
DB_PASSWORD=12345678
```

(You should take the database information from the MySQL section of the docker-compose.yml file and put it exactly as it is into the src/.env file.)

## Run this command for migration

docker compose run --rm project php artisan migrate

## Run this command to run the project

'docker compose up -d'

(it will create mysql folder in root directory)

## Visit the project and open the database server

App Visit: https://localhost/ <br>
Database Visit: https://localhost:8080

## Run other command before adding 'docker compose run --rm project'

Such as:
<br>

1. 'docker compose run --rm project php artisan storage:link'
   <br>
2. 'docker compose run --rm project composer install packagename'
