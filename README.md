## SET UP DOCKER

make setup

make data

## SET UP APACHE CONF

docker exec -it laravel-docker bash

apt-get install vim

vi /etc/apache2/apache2.conf

```
<VirtualHost *:80>
     ServerName dockerlaravel.com
     DocumentRoot /var/www/html/public
     <Directory /var/www/html/public>
         AllowOverride All
         Require all granted
     </Directory>
 </VirtualHost>
```
