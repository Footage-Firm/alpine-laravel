[![](https://images.microbadger.com/badges/image/videoblocks/alpine-laravel.svg)](https://microbadger.com/images/videoblocks/alpine-laravel "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/videoblocks/alpine-laravel.svg)](https://microbadger.com/images/videoblocks/alpine-laravel "Get your own version badge on microbadger.com")

# alpine-laravel
This is a lightweight Docker image optimized for Laravel and built on Alpine Linux. It has a pretty standard setup for PHP 7.1, PHP-FPM, NGINX, and Composer. The PHP extensions are heavily limited to those most commonly used in a Laravel application. It works out of the box, and though future updates are pending, it will remain as small as possible.

## TODOs:
- [] Investigate other PHP extensions that *need* to be added.
- [] Possibly add a global `laravel` installer command.
- [] Possibly add a global `artisan` command.

## Example docker-compose.yml 
```yaml
version: '2.1'
services:
  web:
    image: videoblocks/alpine-laravel:latest
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - ../../:/var/www/html
    working_dir: /var/www/html
```

Note: This is image originally based on https://github.com/TrafeX/docker-php-nginx