# lamp-stack-website-sl3
SOFTWARE LAB-3
Assignment 1
Task-1 :- Create a website using lamp stack.
To accomplish this project first we have to install Linux,Apache,Mysql,PHP(LAMP) on our system. 

Follow this commands to complete the installisation process

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

nano /var/www/your_domain/index.html
Here we have to create a index.html file to test our installing process.
After performing http://raikal this our web page should reflect the content in the file.
In step we have to test PHP processing and data base connection from php.
If our test cases work properly then we can start our project in system.

In our Project we have to create a database by using 
mysql> CREATE DATABASE; Command
mysql> GRANT ALL ON FOOTWEAR.* TO 'raikal’'@'%';
And exiting the root console by exit command
then we see the data bases present in it by using the command .

mysql> SHOW DATABASES;
After executing this command we will see all databases in our mysql
Then we have create a table according to need of our webpage as follows image
![table](https://user-images.githubusercontent.com/100151439/186207872-e94b6efe-4966-48a5-9330-bb3140275c2a.jpeg)

here we created our table then we have write our codes for php files where can impliment add, delete, update functions in our web page.

we have perform gedit * command to run our files in our domain 
after completing php files we see our web page by using 

http://raikal/index.php
here our web page will be opened and we can perform add,delete and update functions
![trl page](https://user-images.githubusercontent.com/100151439/186209373-9c362b61-34a2-4453-bf2c-0297f16c83f4.jpeg)
![updt page](https://user-images.githubusercontent.com/100151439/186209418-4e4a463c-0964-4de2-9188-987a63b40089.jpeg)
After updating we can see that our page is running successfully.
A web page with simple functions using lamp stack is created.

