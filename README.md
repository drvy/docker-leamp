# Docker Compose LEMP / LAMP stack

Simple compose `.yml` files that build a LEMP or a LAMP stack. Intended for development purposes only. I also have a Vagrant Box for development purposes, [check it out here](https://github.com/drvy/drvys-box).


## Services

Services depend on the compose file chosen. In all cases, PHPMyAdmin and MySQL will be available.

- PHPMyAdmin (`phpmyadmin/phpmyadmin`)
- MySQL 5.7 (`mysql:5.7`)

- LEMP74
    - NGINX (`nginx:latest`)
    - PHP 7.4-fpm (`php:7.4-fpm`)
    - PHP Extensions: `xdebug`, `zip`, `gd`, `mysqli`, `curl`, `mysql_pdo`

- LAMP74
    - APACHE & PHP (php-7.4-apache)
    - PHP Extensions: `xdebug`, `zip`, `gd`, `mysqli`, `curl`, `mysql_pdo`


## Install

You must indicate to `docker-compose` the compose file you want to manage at all
times. For example, to build and run a LEMP 7.4 Stack:

1. Clone ( `git clone https://github.com/drvy/docker-lemp.git` )
2. Build ( `docker-compose -f lemp74.yml build --no-cache` )
3. Run   ( `docker-compose -f lemp74.yml up -d` )
4. Use   ( `http://localhost` )


Use the `./src` folder for project files. MySQL is stored in `./docker/db` so it can be persistent. Both `./src` and `./docker/db` are shared between stacks.

### Ports

- __NGINX__ and __APACHE__ are exposed to `80` (80 in their container).
- __PHPMyAdmin__ is exposed to `9192` (80 in it's container).
- __MySQL__ is exposed to `9193` (3306 in it's container).
- __PHPFPM__ is exposed to `9194` (9000 in it's container).

