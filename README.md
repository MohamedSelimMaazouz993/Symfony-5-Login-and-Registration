# Symfony-5-Login-and-Registration

### Setup for the Symfony 5 Login & Registration
---------------------------------------
### 1) composer create-project symfony/website-skeleton:"5.3.x@dev" symfonyAuth
### 2) setup .env file ( go to the line 32 Remove "#" from the database program you will use { choose either Myslq or postgreSql or sql lite}  in this project i used mySql )
### if you had The metadata storage is not up to date error just add the following command in the .env file =
### the name of the db is symfony_auth
### "root: " => Root is the username and blank space is the password because by default in mysql ( password is "" )
###   DATABASE_URL=mysql://root:@127.0.0.1:3306/symfony_auth?serverVersion=mariadb-10.4.11 
### 3) php bin/console doctrine:database:create
### 4) php bin/console make:user
### 5) php bin/console make:migration
### 6) php bin/console doctrine:migrations:migrate
### 7) php bin/console make:auth
### 8) php bin/console make:registration
### there will an error due to there is no eouter for the redirecting page
### just remove // from the line 54 and change (your_app) to (app_login )  
### also add // to the line 55 " throw new execption "
### 9) symfony serve
### And the project will work like charm :D
