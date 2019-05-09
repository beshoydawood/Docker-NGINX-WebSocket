# Docker NGINX WebSocket (PHP7-FPM - NGINX - MySQL - ELK)

Docker NGINX WebSocket is a complete docker container 
for general PHP developments, Mainly it was created to implement websockets with nginx and provide ready solution to create Docker TCP server 

## Installation

1. Create a `.env` from the `.env.dist`

    ```bash
    cp .env.dist .env
    ```

2. Build/run containers with (with and without detached mode)

    ```bash
    $ docker-compose build
    ```
3. Once the build is done just run compass-watch file the (.bat) file for Windows and (.applescript) for mac users, If you are on linux run the following command:

    ```bash
    $  docker-compose up -d
    ```
4. Enjoy :-)

## Usage

Just run `docker-compose up -d`, then:

* Visit [localhost](http://localhost) you should see
`phpinfo()`
* Place your app files inside www folder
* The WS server is avilablae on port 8888 [ws://localhost:8888](ws://localhost:8888)  
* Logs (Kibana): (http://localhost:81/)
* Logs (files location): logs/nginx 

## Useful commands
```bash
# PHP commands 
$ docker-compose exec php bash
# Fire up the PHP WS server file
$ php -q /www/WS_SERVER.PHP

# MySQL commands
$ docker-compose exec db mysql -uroot -p"root"

# Nginx commands
$ docker-compose exec nginx bash
```
## General Notes

Nginx is built from debian:jessie with PHP 7.1-FPM if you would like to use different PHP version update the docker file inside PHP folder, This container was created for educational purpose you can't use it in live production without little tweaks.
