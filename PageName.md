# Introduction #

php5rp is a simple reverse proxy written in PHP. It's a stub, and doesn't follow all RFCs.


# Usage #

### Apache Config ###
```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f [NC]
RewriteCond %{REQUEST_FILENAME} !-d [NC]
RewriteCond %{REQUEST_URI} !^/index.php
RewriteRule ^(.+)$ index.php/$1 [QSA]
```
### Simple Usage ###
```
$proxy = new ProxyHandler('http://publicsite.example.com','http://privatesite.example.com');
$proxy->execute();
```