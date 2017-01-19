#Réseau-Système

##Comment interagissent les logiciels
° Le client envoie une requête url depuis son navigateur au serveur Apache via internet

° Le serveur sql interroge le serveur base de données Mysql via php

° Mysql renvoie ce que php lui demande, et php interprète en html

° PHP renvoie au serveur Apache qui transmet au client en html

##Rôle du serveur web
° Un serveur comprend des logiciels (Apache, php, Mysql) qui fonctionnent ensemble. 

° Il permet de stocker les fichiers d’un site web et de contrôler la façon dont les utilisateurs peuvent y accéder.

##Démarche utilisée pour installer l’ensemble
° Recherche de tutoriels

° Connexion au server avec un code ssh root@vpsxxx.ovh.net

° apt get update, apt get upgrade, apt install apache2

° Test →  /var/www/html/index.html

° apt get install .php5

° Création d’un test pour le lancer sur le server et l’afficher dans le navigateur → nano test.php

° apt get update, apt get upgrade, apt install my-sql-server

° Changement du mot de passe pour Mysql, puis confirmation

° Test → /etc/init.d/mysql status

° SHOW DATABASE ;

° Copie du dossier Code_Closet : scp -R code-closet  /var/www/html

° Changement des droits du dossier : chmod

° Activation du mode Rewrite Apache (recherche Google) a2enmod rewrite : pour rechercher automatiquement la page index.php ; config dans .htaccess dans public laravel

° Répertoire public → sites-enabled/000-default.conf

° Debug var/log/apache2/error.log → laravel.log

° Configurer Apache (dans le virtualhost) pour arriver sur  var/www/html/../public/index.php
