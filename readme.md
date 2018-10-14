<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"> <h1>vs</h1>
<img src="https://www.docker.com/sites/default/files/horizontal.png"></p>

[Youttube Video](https://opensource.org/licenses/MIT)

## Init
-Scarica Docker
-Scarica laravel project
-Scarica Laradock
-Copia laradock nella dir del project laravel
-Spostati nella dir laravel e copia il file .env  : mv .envexample .env
-Configura .env Laradock Sezione MYSQL
-Configura .env Laravel Sezione MYSQL

Lancia Docker
        docker-compose up -d  //start containers

Indirizzo : 127.0.0.1 trovi il site       

docker-compose stop o docker-compose kill


## Database
docker exec -it alias_mysql bash

mysql -uroot -proot

-Incolla questo codice modificando con nome db e tupassword uguali a quello che ha scritto nei file env

CREATE USER 'admin'@'localhost' IDENTIFIED WITH mysql_native_password BY 'tuapassword';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;
CREATE USER 'admin'@'%' IDENTIFIED WITH mysql_native_password BY 'tuapassword';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'%' WITH GRANT OPTION;
#
CREATE DATABASE IF NOT EXISTS `isjeadydocker` COLLATE 'utf8_general_ci' ;
GRANT ALL ON `isjeadydocker`.* TO 'admin'@'%' ;
FLUSH PRIVILEGES ;


-Crea la connessione con mysql workbanch

## Esegeui 

-docker exec -it alias_workspace bash

-php artisan migrate 

-Dovresti aver terminato.

Isjeady 
  
