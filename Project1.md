![Screen Shot 2021-04-07 at 4 15 39 PM](https://user-images.githubusercontent.com/82106518/113891049-9dadf000-97bc-11eb-9f9e-63a332ef1651.png)
![Screen Shot 2021-04-07 at 4 15 03 PM](https://user-images.githubusercontent.com/82106518/113891395-f3829800-97bc-11eb-88ec-c28ff4759772.png)
![image](https://user-images.githubusercontent.com/82106518/113892192-af43c780-97bd-11eb-83e2-f3db31eab274.png)
![image](https://user-images.githubusercontent.com/82106518/113892221-b79c0280-97bd-11eb-8f20-f6c23ebb7b8b.png)

sudo apt install mysql-server
sudo mysql_secure_installation
sudo apt install php libapache2-mod-php php-mysql
php -v

$ sudo mkdir /var/www/projectdevops
sudo chown -R $USER:$USER /var/www/projectlamp
$ sudo vi /etc/apache2/sites-available/projectlamp.conf


ServerName projectdevops
    ServerAlias www.projectdevops
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectdevops
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined

sudo ls /etc/apache2/sites-available
sudo a2ensite projectlamp
sudo a2dissite 000-default
sudo apache2ctl configtest
sudo systemctl reload apache2
sudo vim /etc/apache2/mods-enabled/dir.conf
vim /var/www/projectlamp/index.php

