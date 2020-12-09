# Docker Compose configuration for Laravel

### SERVER INFOMATION
* Nginx
* PHP 7.3
* MySQL
* phpMyAdmin

### RUN
```sh
docker-compose build
docker-compose up

# Attach shell
docker-compose exec php-fpm bash

```

### Laravel Setup
```sh
composer install

cp .env.example .env

# Edit database configuration within .env file as below:
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laraveldb
DB_USERNAME=laraveluser
DB_PASSWORD=password

# Generate key
php artisan key:generate

# Migrate DB
php artisan migrate
```
### Show result
## Open web browser
 - Laravel: `localhost:8000`
 - phpMyAdmin: `localhost: 8081`

Good luck
