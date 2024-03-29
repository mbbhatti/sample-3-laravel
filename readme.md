## About
LMS based Application. 

## Requirments
- PHP >= 7.2
- Laravel >= 6.2
- MySql >= 5.6

## Installation 
Laravel utilizes composer to manage its dependencies. So, before using Laravel, make sure you have composer installed on your machine. To download all required packages run these commands or you can download [Composer](https://getcomposer.org/doc/00-intro.md).
- composer install

## Database Setup
You need to create a .env file from. env.example, if .env not exists.
-  cp .env.example .env

Then, run this command to create key in .env file if not exists.
- php artisan key:generate

Now, set your database credential against these in .env file.

- DB_CONNECTION=mysql
- DB_HOST=127.0.0.1
- DB_PORT=3306
- DB_DATABASE=homestead
- DB_USERNAME=homestead
- DB_PASSWORD=secret

Use this migration command to create database tables and fake entries.
- php artisan migrate:refresh --seed

You can download digram [Scheme](https://github.com/mbbhatti/databases/blob/master/NeuroNation.png) to view its presentaion.

-Note: History trigger created for histroy table to manage user session categories on insert data into the score table.

## How To Test
PHPUnit used for code testability and performance. You may need to run below commands for testing within php interface.

Use this command for single file
- vendor/bin/phpunit --filter [FileName]

Use this command for all files tests
- vendor/bin/phpunit

## How To Run
- php artisan serve