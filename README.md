# lamp-stack-website-sl3
SOFTWARE LAB-3
Assignment 1
Task-1 :- Create a website using lamp stack.
The first step starts with installing the Linux,Apache,MySQL,PHP(LAMP) in the ubuntu by using the commands like

$ sudo apt update
$sudo apt install apache2
$ sudo ufw app list
$ sudo ufw allow in "Apache"
After completing by using the http://server_ip (the server ip can be known by ifconfig command.)we get  Apache web page.
And coming to mySQL we use following commands

$sudo apt install mysql-server
$sudo mysql_secure_installation

So it asks for password reset so we proceed further by fixing password.
And next is PHP installation by commands
$ sudo apt install php libapache2-mod-php php-mysql
$ php -v

After we will create a virtual host by following commands

$ sudo mkdir /var/www/raikal
$ sudo chown -R $USER:$USER /var/www/raikal
$ sudo nano /etc/apache2/sites-available/raikal.conf
$ sudo a2ensite raikal
$ sudo a2dissite 000-default
$sudo apache2ctl configtest
$ sudo systemctl reload apache2
