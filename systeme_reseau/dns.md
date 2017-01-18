# Titre 1

## Titre 2

test 


```
<VirtualHost *:80>
        DocumentRoot /var/www/carmelina.napolitano
        ServerName carmelina.code-closet.com
RewriteEngine on
RewriteCond %{SERVER_NAME} =carmelina.code-closet.com
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,QSA,R=permanent]
</VirtualHost>

```
