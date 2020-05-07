# How to Setup a Laravel Project You Cloned from Github.com

## 1. Clone GitHub repo for this project locally
git clone linktogithubrepo.com/ projectName

## 2. cd into your project
You will need to be inside that project file to enter all of the rest of the commands

## 3. [Optional]: Checkout the “Start” tag so you have a fresh install of the project (and not the final files)
git checkout tags/start -b tutorial

## 4. Install Composer Dependencies
composer install

## 5. Install NPM Dependencies
npm install
or if you prefer yarn (as i do)
yarn

then yarn run dev or production

## 6. Create a copy of your .env file
cp .env.example .env

## 7. Generate an app encryption key
php artisan key:generate

## 8. Create an empty database for our application
Create an empty database for your project using the database tools you prefer

## 9. In the .env file, add database information to allow Laravel to connect to the database
In the .env file fill in the DB_HOST, DB_PORT, DB_DATABASE, DB_USERNAME, and DB_PASSWORD options to match the credentials of the database you just created. This will allow us to run migrations and seed the database in the next step.

## 10. Migrate the database
php artisan migrate

## 11. [Optional]: Seed the database
php artisan db:seed
( If the repo doesn’t mention the existence of a seeder file, then skip this step. )
