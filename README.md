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

# Attach shel
docker-compose exec php-fpm bash

```

### Laravel Queue
```sh
composer install
php artisan key:generate
php artisan migrate
```
### Show result

Open browser
Laravel: localhost:8000
phpMyAdmin: localhost: 8081

Good luck
