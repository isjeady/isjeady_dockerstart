<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>
<p align="center"><img src="https://www.docker.com/sites/default/files/horizontal.png"></p>

Isjeady Youtube Video [Youtube](https://www.youtube.com/channel/UC1fhZ1C2E-UOZjeIvm1XpWw) e [isjeady.com](https://isjeady.com) 

## Init
- Scarica Docker
- Scarica laravel project
- Scarica Laradock
- Copia laradock nella dir del project laravel
- Spostati nella dir laravel e copia il file .env  ```mv .envexample .env```
- Configura .env Laradock Sezione MYSQL
- Configura .env Laravel Sezione MYSQL

***Lancia Docker***
``` docker-compose up -d  //start containers```

Indirizzo : 127.0.0.1 trovi il site       
```
docker-compose stop 

docker-compose kill

```
## Database
```
docker exec -it alias_mysql bash
```
- -***Per accedere alla console interna mysql ***
```
mysql -uroot -proot
```

- Incolla questo codice modificando con nome db e tupassword uguali a quello che ha scritto nei file env

```
CREATE USER 'admin'@'localhost' IDENTIFIED WITH mysql_native_password BY 'tuapassword';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;
CREATE USER 'admin'@'%' IDENTIFIED WITH mysql_native_password BY 'tuapassword';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'%' WITH GRANT OPTION;
#
CREATE DATABASE IF NOT EXISTS `isjeadydocker` COLLATE 'utf8_general_ci' ;
GRANT ALL ON `isjeadydocker`.* TO 'admin'@'%' ;
FLUSH PRIVILEGES ;
```


- Crea la connessione con ***mysql workbanch***

## Esegui 
```
-docker exec -it alias_workspace bash

-php artisan migrate 
```

Dovresti aver terminato.
Se hai problemi di accesso al Db puoi provare a creare l'utenza direttamente da mysql workbanch.

***All code released under the [MIT License](https://opensource.org/licenses/MIT)***
  
