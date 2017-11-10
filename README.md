# alpine-laravel
A Laravel optimized Docker image using Alpine Linux.

## Example docker-compose.yml 
```yaml
version: '2.1'
services:
  web:
    image: videoblocks/bannister-web:latest
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - ../../:/var/www/html
    working_dir: /var/www/html
```

Note: This is image originally based on https://github.com/TrafeX/docker-php-nginx