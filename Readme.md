# 🐳 Docker + PHP 8.0.3 + MySQL + Nginx + Symfony 5 

## Description

This is a complete stack for running Symfony 5 into Docker containers using docker-compose tool.

It is composed by 3 containers:

- `nginx`, acting as the webserver.
- `php`, the PHP-FPM container with the 7.4 PHPversion.
- `db` which is the MySQL database container with a **MySQL 8.0** image.

## Installation

1. Run `docker-compose up -d`

2. The 3 containers are deployed: 

```
Creating symfony-docker_db_1    ... done
Creating symfony-docker_php_1   ... done
Creating symfony-docker_nginx_1 ... done
```

3. Use this command to migrate the db: docker exec -t symfony-docker_php_1 bin/console doctrine:migrations:migrate --env=prod --no-interaction

