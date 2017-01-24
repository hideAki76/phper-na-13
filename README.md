# phper-na #13

## local #1
    $ mkdir wordpress
    $ cd wordpress
    $ git clone https://github.com/hideAki76/phper-na-13.git
    $ docker-compose up -d
    $ docker exec -it wordpress_php_1 /bin/bash -c 'su - phper'
    phper

## docker container #1
    container$ git clone https://github.com/torounit/composer-wp-dev-kit.git
    container$ exit

## local #2
    $ cp local-config.json www/composer-wp-dev-kit/
    $ cp provision.sh www/composer-wp-dev-kit/bin/
    $ cp server.sh www/composer-wp-dev-kit/bin/
    $ docker exec -it wordpress_php_1 /bin/bash -c 'su - phper'

## docker container #2
    container$ cd composer-wp-dev-kit
    container$ composer install
    container$ composer provision
    container$ ./bin/server.sh

## browser
http://localhost:9000/
