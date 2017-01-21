# phper-na #13

## local #1
    $ mkdir wordpress
    $ cd wordpress
    $ git clone https://github.com/hideAki76/phper-na-13.git
    $ docker-compose up -d
    $ docker exec -it wordpress_php_1 /bin/bash -c 'su - phper'
    phper

## docker container #1
    container$ composer create-project torounit/composer-wp-dev-kit .
    container$ exit

## local #2
    $ cp local-config.json www/
    $ cp provision.sh www/bin/
    $ cp server.sh www/bin/
    $ docker exec -it wordpress_php_1 /bin/bash -c 'su - phper'

## docker container #2
    container$ composer provision
    container$ ./bin/server.sh

## browser
http://localhost:9000/
