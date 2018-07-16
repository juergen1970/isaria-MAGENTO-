# isaria-MAGENTO-
E-Shop for Isaria

Install-Options:
- Windows 10
- Ubuntu 16.04 LTS

Published:
WebPage: isaria.ddns.net
Hardware: Raspberry Pi


Install apache mysql php magento 2 ubuntu 16.04
System Requirements: http://devdocs.magento.com/magento-system-requirements.html
 
$ sudo apt-get install apache2
http://localhost/ => working
$ sudo apt-get install mysql-server
$ mysql_secure_installation
 
php:
$ sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql php-soap
 
php - module
$ sudo apt-get install php-gd php-curl php-intl php-mbstring php-zip php-dom php-xsl php-simplexml

#Nach PHP Installation:
sudo ln -s /etc/phpmyadmin/apache.conf /etc/apache2/conf-available/phpmyadmin.conf
sudo a2enconf phpmyadmin.conf
sudo systemctl reload apache2.service

User: root
PW: YES

mod-rewrite
$ a2enmod rewrite
edit file
$ subl /etc/apache2/apache2.conf (if you dont have sublime text use gedit /etc/apache2/apache2.conf, or nano /etc/apache2/apache2.conf)
Find the line with <Directory /var/www> then change  AllowOverride to All
 
$ sudo service apache2 restart
 
composer
$ sudo apt-get install composer
 
phpmyadmin https://www.phpmyadmin.net/downloads/
 
? In your terminal navigate to phpmyadmin folder and copy this file. type:
? $ cp config then press the tab, config.inc.php
? $ nano config.inc.php
? find the line with blowfish_secret then input 32 random characters, it can be less than 32 but there will be a warning ???
 
Download Magento 2: www.magento.com

and copy extracted folder to: /var/www/html
  
sudo chmod -R 777 var/pub/app/etc

http://localhost/magento2/setup

sublime text 3
https://www.sublimetext.com/3

http://devdocs.magento.com/guides/v2.1/install-gde/system-requirements-tech.html
