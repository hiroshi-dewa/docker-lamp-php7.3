# docker-lamp
Dockerand docker-compose

- Apache (current version: 2)
	- mod_rewrite
	- GD (current version: 2)
- php 7.3
- MySql 5.7
- PhpMyAdmin

* Operation check
  - php7.3
    - ✅ baserCMS 4.3.4

## Advance preparation

- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [Docker Compose](https://docs.docker.com/compose/install/)

## How to set up

```
$ cd dockker-lamp-php7.3
$ docker-compose build
$ docker-compose up
```

You can access [http://localhost:8080/](http://localhost:8080/)

## Directory

```
├ public_html : Document root
├ docker-compose.yml
└ docker
  ├ web
    ├ Dockerfile : php veersion, apache install
    ├ base.conf : <VirtualHost *:80>
    ├ php.ini
  ├ db
    ├ Dockerfile : mysql install
    ├ my.cnf
  ├ logs : server log
```


## MySQL

phpMyAdmin : [http://localhost:8088/](http://localhost:8088/)

- database host : 192.168.202.2 (default)
- database user : root
- database pass : root
- database port : 3306