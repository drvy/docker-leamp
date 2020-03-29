# Docker Compose LAMP stack

Simple `docker-compose.yml` that builds a LAMP stack. Intended for development purposes only. I also have a Vagrant Box for development purposes, [check it out
here](https://github.com/drvy/drvys-box).


## Services

- Apache with PHP 7.4 (`php:7.4-apache`)
- PHPMyAdmin (`phpmyadmin/phpmyadmin`)
- MySQL 5.7 (`mysql:5.7`)
- PHP Extensions: `xdebug`, `zip`, `gd`, `mysqli`, `curl`, `pdo_mysql`
- Apache enabled mods: `mod_rewrite`

## Install

1. Clone ( `git clone https://github.com/drvy/docker-lemp.git` )
2. Switch ( `git checkout -b LEMP-74` )
2. Build ( `docker-compose build --no-cache` )
3. Run   ( `docker-compose up -d` )
4. Use   ( `http://localhost` )

### Ports

- __APACHE__ is exposed to `80` (80 in it's container).
- __PHPMyAdmin__ is exposed to `9192` (80 in it's container).
- __MySQL__ is exposed to `9193` (3306 in it's container).

### Info

MySQL is stored in `./docker/db` so it can be persistent.
