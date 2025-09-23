# Laravel-Docker-Alin-Version

Laravel-Docker-Alin-Version is a pre-built and customizable Docker environment for Laravel. With this setup, you can quickly create and manage Laravel projects inside Docker without complex configurations.

This project was originally customized by Masum, and later further adapted and refined by me to match my own development needs.

## Last Modifed Date

20-September-2025 by Alin

## Run this command in the terminal for making structure

composer global require laravel/installer

## Run this command in the terminal to Create a Laravel project in 'src' folder

laravel new src

## Modify '.env' file from 'src' folder

```
APP_URL=https://localhost
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=testx
DB_USERNAME=masum
DB_PASSWORD=K4hvdq9tj9
```

(You should take the database information from the MySQL section of the docker-compose.yml file and put it exactly as it is into the src/.env file.)

## Run docker compose up -d

(it will create mysql folder in root directory)

## Visit the project and open the database server

App Visit: https://localhost/ <br>
Database Visit: https://localhost:8080

## Run other command before adding 'docker compose run --rm project'

Such as: 'docker compose run --rm projefct php artisan storage:link'
<br>
or 'docker compose run --rm project compose install packagename'
