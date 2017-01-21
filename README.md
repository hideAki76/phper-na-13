# phper-na-13

## local
    $ mkdir wordpress
    $ cd wordpress
    $ git clone https://github.com/hideAki76/phper-na-13.git
    $ docker-compose up -d
    $ docker exec -it wordpress_php_1 /bin/bash -c 'su - phper'
    phper

## docker container
    container$ composer provision
    container$ exit
## local
    $ cp local-config.json www/
    $ docker exec -it wordpress_php_1 /bin/bash -c 'su - phper'

## docker container
    container$ ./bin/server.sh

## browser
http://localhost:9000/
