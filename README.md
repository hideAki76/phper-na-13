# phper-na #13 ハンズオン環境構築

## ホストOS（windows,mac,linux）での準備作業
    $ mkdir wordpress
    $ cd wordpress
    $ git clone https://github.com/hideAki76/phper-na-13.git
    $ docker-compose up -d
    $ docker exec -it wordpress_php_1 /bin/bash -c 'su - phper'
    パスワード：phper

## dockerコンテナ内での準備作業
    container$ composer create-project torounit/composer-wp-dev-kit .
    container$ mv composer-wp-dev-kit/* .
    container$ composer provision

### docker toolbox の場合
    container$ exit
    $ cp local-config.json www/
    $ docker exec -it wordpress_php_1 /bin/bash -c 'su - phper'
    $ php -S 0.0.0.0:9000

    ブラウザで確認　http://192.168.99.100:9000/

### docker for mac の場合
    container$ ./bin/server.sh

    ブラウザで確認　http://localhost:9000/
