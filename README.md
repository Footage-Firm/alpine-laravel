[![](https://images.microbadger.com/badges/image/videoblocks/alpine-laravel.svg)](https://microbadger.com/images/videoblocks/alpine-laravel "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/videoblocks/alpine-laravel.svg)](https://microbadger.com/images/videoblocks/alpine-laravel "Get your own version badge on microbadger.com")

# alpine-laravel
A Laravel optimized Docker image using Alpine Linux.

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