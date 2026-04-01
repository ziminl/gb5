# gb5


https://www.apachefriends.org



https://github.com/gnuboard/gnuboard5


#win
: path : C:\xampp\mysql\bin

+ sql root 1234

sql admin -> make db g5

and import from C:\xampp\htdocs\install\gnuboard5shop.sql

mysql -u root -p

CREATE USER <usrname>;

GRANT ALL PRIVILEGES ON g5.* to '<usrname>'@'%' identified by '<password>';


# community to shop

in

theme/테마명/theme.config.php 

define('G5_COMMUNITY_USE', false);


# enable gd 

php.ini -> ;extension=gd to extension=gd
