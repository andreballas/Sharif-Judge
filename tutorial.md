# Tutorial for Installing PCSJudge in a Linux Distro




### Part 1 - Setting up your environment
- Install a Linux distro
- Install the LAMP package - Apache2, PHP7 and Postgres. Make sure that your current version is PHP7 typing:
```sh
$ php -v
```
- Check if it is all right with Apache installation just typing your server address in your browser, e.g., 
```sh
127.0.0.1
```
- Install p7zip-full package
```sh
apt-get install p7zip-full
```



### Part 2 - Downloading SharifJudge
- Download SharifJudge from PCS' Github repository
- Move the folder to this directory (or your predefined server folder)
```sh
var/www/html 
```
- Unzip it
- Edit index.php and change it to development mode




### Part 3 - Setting up a database
Access postgres's shell by typing (where **** is your password defined at the postgres's installation process)
```sh
$ sudo -u postgres psql
```
- Create a database for the Judge typing 
```sh
$ create database Judge;
```
- Exit the shell by typing 
```sh
$ exit
```



### Part 4 - Setting up SharifJudge
- in your Judge folder, edit setting the parameters needed as the instructions show
```sh
/application/config/database.php 
```
- Give to Twig folder access to be writable by PHP 
```sh
$ chown -R www-data:www-data /application/cache/Twig
```
- In /application/config/config.php change line 42 to set the base_url as the URL for the website

- Type in you browser and follow all the instructions
```sh
localhost/Judge/index.php 
```
- it will be needed to move assignments and tester folders to another directory and give them the same permission as you did for Twig

###### OBS: Do not forget to install g++ for compiling C++ code!

