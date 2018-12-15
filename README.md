# Laravel Project

## Prolog

Pull new project from here. Laravel version = 5.7

## Set Up

### Installation
1. Install composer, mysql<br>
Ubuntu : https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-16-04<br>
Windows : http://webdevzoom.com/how-to-install-composer-on-windows/<br>
http://www.tomshardware.com/faq/id-3682255/install-mysql-windows.html

### Get the project
2. Make an empty directory for the project
3. In the empty directory, run this command to pull the project :
```
git init
git remote add origin https://github.com/drestanto/laravel_new_project.git
git pull origin master
```
  Input your gitlab username and password
4. Install composer inside the project :
```
composer install
```

### Database Set-up
5. Open mysql, make a new database :
```
CREATE DATABASE database_name
```
6. Make .env file inside the directory. Copy everything from the .env.example <br>
   Setup your DB_DATABASE, DB_USERNAME, and DB_PASSWORD <br>
   Set APP_KEY=base64:CkaIOp8tWWYvDrn/hV7OaDyP7wAtjpq7BZfYowH+m7o=<br>
   Set Email
```
	MAIL_DRIVER=smtp
	MAIL_HOST=smtp.gmail.com
	MAIL_PORT=587
	MAIL_USERNAME=youremail@web.com
	MAIL_PASSWORD=yourpassword
	MAIL_ENCRYPTION=tls
```
In this step, choose either one :
* If you want a new one (a clean database) <br>
Migrate from the project, run artisan command :
```
php artisan migrate
```

* If you want to use existing mock up database <br>
Copy database from simpensql.sql to your database :
```
mysql -u username -p database_name < simpensql.sql
```
Input your mysql password


### Run the program
8. Run artisan command :
```
php artisan serve
```
9. Open browser, link = localhost:8000

<hr>

## Tutorial

https://laravel.com/docs/5.7/