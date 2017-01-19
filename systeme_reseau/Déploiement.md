```
carmelina.napolitano@PC-DG-CAMPUS-22 MINGW64 /
$ ssh root@code-closet.com
root@code-closet.com's password:

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Thu Jan 19 13:23:24 2017 from 89.227.215.1
root@vps355203:~# cd /etc/apache2/
root@vps355203:/etc/apache2# ls
apache2.conf  conf-available  conf-enabled  envvars  magic  mods-available  mods-enabled  ports.conf  sites-available  sites-enabled
root@vps355203:/etc/apache2# cd sites-enabled/
root@vps355203:/etc/apache2/sites-enabled# ls
carmelina.conf  carmelina-le-ssl.conf  code-closet.conf  germain.conf  loic.conf  loic-le-ssl.conf  loic.maupin.conf  sergio.conf  serg
root@vps355203:/etc/apache2/sites-enabled# cat carmelina.conf
<VirtualHost *:80>
        DocumentRoot /var/www/carmelina.napolitano
        ServerName carmelina.code-closet.com
RewriteEngine on
RewriteCond %{SERVER_NAME} =carmelina.code-closet.com
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,QSA,R=permanent]
</VirtualHost>

root@vps355203:/etc/apache2/sites-enabled# cd /var/www/carmelina.napolitano
root@vps355203:/var/www/carmelina.napolitano# ls
index.php
root@vps355203:/var/www/carmelina.napolitano# cat
^C
root@vps355203:/var/www/carmelina.napolitano# cat index.php
<?php echo 'Hello Carmelina';
root@vps355203:/var/www/carmelina.napolitano# rm index.php
root@vps355203:/var/www/carmelina.napolitano# ls
root@vps355203:/var/www/carmelina.napolitano# git clone https://github.com/campus-digital-grenoble/code-closet.git
Cloning into 'code-closet'...
fatal: unable to access 'https://github.com/campus-digital-grenoble/code-closet.git/': Could not resolve host: github.com
root@vps355203:/var/www/carmelina.napolitano# git clone https://github.com/campus-digital-grenoble/code-closet.git
Cloning into 'code-closet'...
fatal: unable to access 'https://github.com/campus-digital-grenoble/code-closet.git/': Could not resolve host: github.com
root@vps355203:/var/www/carmelina.napolitano# cat /etc/host
cat: /etc/host: No such file or directory
root@vps355203:/var/www/carmelina.napolitano# cat /etc/hosts
127.0.0.1       localhost
51.255.51.212   vps355203.ovh.net       vps355203
root@vps355203:/var/www/carmelina.napolitano#
root@vps355203:/var/www/carmelina.napolitano# nslookup github.com
-bash: nslookup: command not found
root@vps355203:/var/www/carmelina.napolitano# apt-get install net-utils
Reading package lists... Done
Building dependency tree
Reading state information... Done
E: Unable to locate package net-utils
root@vps355203:/var/www/carmelina.napolitano# apt-get install netutils
Reading package lists... Done
Building dependency tree
Reading state information... Done
E: Unable to locate package netutils
root@vps355203:/var/www/carmelina.napolitano# apt-get install net-tools
Reading package lists... Done
Building dependency tree
Reading state information... Done
net-tools is already the newest version.
0 upgraded, 0 newly installed, 0 to remove and 52 not upgraded.
root@vps355203:/var/www/carmelina.napolitano# apt-get install nettools
Reading package lists... Done
Building dependency tree
Reading state information... Done
E: Unable to locate package nettools
root@vps355203:/var/www/carmelina.napolitano# apt-get install netools
Reading package lists... Done
Building dependency tree
Reading state information... Done
E: Unable to locate package netools
root@vps355203:/var/www/carmelina.napolitano# apt-get install dnsutils
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following extra packages will be installed:
  bind9-host geoip-database libbind9-90 libdns100 libgeoip1 libisc95 libisccc90 libisccfg90 liblwres90
Suggested packages:
  rblcheck geoip-bin
The following NEW packages will be installed:
  bind9-host dnsutils geoip-database libbind9-90 libdns100 libgeoip1 libisc95 libisccc90 libisccfg90 liblwres90
0 upgraded, 10 newly installed, 0 to remove and 52 not upgraded.
Need to get 2,834 kB of archives.
After this operation, 8,639 kB of additional disk space will be used.
Do you want to continue? [Y/n] Y
Get:1 http://ftp.debian.org/debian/ jessie/main libgeoip1 amd64 1.6.2-4 [90.8 kB]
Get:2 http://ftp.debian.org/debian/ jessie/main geoip-database all 20150317-1 [1,517 kB]
Get:3 http://security.debian.org/ jessie/updates/main libisc95 amd64 1:9.9.5.dfsg-9+deb8u9 [169 kB]
Get:4 http://security.debian.org/ jessie/updates/main libdns100 amd64 1:9.9.5.dfsg-9+deb8u9 [682 kB]
Get:5 http://security.debian.org/ jessie/updates/main libisccc90 amd64 1:9.9.5.dfsg-9+deb8u9 [36.5 kB]
Get:6 http://security.debian.org/ jessie/updates/main libisccfg90 amd64 1:9.9.5.dfsg-9+deb8u9 [57.1 kB]
Get:7 http://security.debian.org/ jessie/updates/main libbind9-90 amd64 1:9.9.5.dfsg-9+deb8u9 [43.3 kB]
Get:8 http://security.debian.org/ jessie/updates/main liblwres90 amd64 1:9.9.5.dfsg-9+deb8u9 [52.9 kB]
Get:9 http://security.debian.org/ jessie/updates/main bind9-host amd64 1:9.9.5.dfsg-9+deb8u9 [67.6 kB]
Get:10 http://security.debian.org/ jessie/updates/main dnsutils amd64 1:9.9.5.dfsg-9+deb8u9 [119 kB]
Fetched 2,834 kB in 10s (278 kB/s)
Selecting previously unselected package libgeoip1:amd64.
(Reading database ... 50620 files and directories currently installed.)
Preparing to unpack .../libgeoip1_1.6.2-4_amd64.deb ...
Unpacking libgeoip1:amd64 (1.6.2-4) ...
Selecting previously unselected package libisc95.
Preparing to unpack .../libisc95_1%3a9.9.5.dfsg-9+deb8u9_amd64.deb ...
Unpacking libisc95 (1:9.9.5.dfsg-9+deb8u9) ...
Selecting previously unselected package libdns100.
Preparing to unpack .../libdns100_1%3a9.9.5.dfsg-9+deb8u9_amd64.deb ...
Unpacking libdns100 (1:9.9.5.dfsg-9+deb8u9) ...
Selecting previously unselected package libisccc90.
Preparing to unpack .../libisccc90_1%3a9.9.5.dfsg-9+deb8u9_amd64.deb ...
Unpacking libisccc90 (1:9.9.5.dfsg-9+deb8u9) ...
Selecting previously unselected package libisccfg90.
Preparing to unpack .../libisccfg90_1%3a9.9.5.dfsg-9+deb8u9_amd64.deb ...
Unpacking libisccfg90 (1:9.9.5.dfsg-9+deb8u9) ...
Selecting previously unselected package libbind9-90.
Preparing to unpack .../libbind9-90_1%3a9.9.5.dfsg-9+deb8u9_amd64.deb ...
Unpacking libbind9-90 (1:9.9.5.dfsg-9+deb8u9) ...
Selecting previously unselected package liblwres90.
Preparing to unpack .../liblwres90_1%3a9.9.5.dfsg-9+deb8u9_amd64.deb ...
Unpacking liblwres90 (1:9.9.5.dfsg-9+deb8u9) ...
Selecting previously unselected package bind9-host.
Preparing to unpack .../bind9-host_1%3a9.9.5.dfsg-9+deb8u9_amd64.deb ...
Unpacking bind9-host (1:9.9.5.dfsg-9+deb8u9) ...
Selecting previously unselected package dnsutils.
Preparing to unpack .../dnsutils_1%3a9.9.5.dfsg-9+deb8u9_amd64.deb ...
Unpacking dnsutils (1:9.9.5.dfsg-9+deb8u9) ...
Selecting previously unselected package geoip-database.
Preparing to unpack .../geoip-database_20150317-1_all.deb ...
Unpacking geoip-database (20150317-1) ...
Processing triggers for man-db (2.7.0.2-5) ...
Setting up libgeoip1:amd64 (1.6.2-4) ...
Setting up libisc95 (1:9.9.5.dfsg-9+deb8u9) ...
Setting up libdns100 (1:9.9.5.dfsg-9+deb8u9) ...
Setting up libisccc90 (1:9.9.5.dfsg-9+deb8u9) ...
Setting up libisccfg90 (1:9.9.5.dfsg-9+deb8u9) ...
Setting up libbind9-90 (1:9.9.5.dfsg-9+deb8u9) ...
Setting up liblwres90 (1:9.9.5.dfsg-9+deb8u9) ...
Setting up bind9-host (1:9.9.5.dfsg-9+deb8u9) ...
Setting up dnsutils (1:9.9.5.dfsg-9+deb8u9) ...
Setting up geoip-database (20150317-1) ...
Processing triggers for libc-bin (2.19-18+deb8u6) ...
root@vps355203:/var/www/carmelina.napolitano#
root@vps355203:/var/www/carmelina.napolitano# git clone https://github.com/campus-digital-grenoble/code-closet.git
Cloning into 'code-closet'...
Username for 'https://github.com': anilemraC
Password for 'https://anilemraC@github.com':
fatal: unable to access 'https://github.com/campus-digital-grenoble/code-closet.git/': Could not resolve host: github.com
root@vps355203:/var/www/carmelina.napolitano# nslookup github.com
Server:         213.186.33.99
Address:        213.186.33.99#53

Non-authoritative answer:
Name:   github.com
Address: 192.30.253.112
Name:   github.com
Address: 192.30.253.113

root@vps355203:/var/www/carmelina.napolitano# nslookup github.com
Server:         213.186.33.99
Address:        213.186.33.99#53

Non-authoritative answer:
Name:   github.com
Address: 192.30.253.113
Name:   github.com
Address: 192.30.253.112

root@vps355203:/var/www/carmelina.napolitano# nslookup github.com
^C
root@vps355203:/var/www/carmelina.napolitano# nslookup github.com
^C
root@vps355203:/var/www/carmelina.napolitano# emacs /etc/hosts

[1]+  Stopped                 emacs /etc/hosts
root@vps355203:/var/www/carmelina.napolitano# ^C
root@vps355203:/var/www/carmelina.napolitano# fg
emacs /etc/hosts
root@vps355203:/var/www/carmelina.napolitano# emacs /etc/hosts
root@vps355203:/var/www/carmelina.napolitano# nslookup github.com
Server:         213.186.33.99
Address:        213.186.33.99#53

Non-authoritative answer:
Name:   github.com
Address: 192.30.253.112
Name:   github.com
Address: 192.30.253.113

root@vps355203:/var/www/carmelina.napolitano# fg
root@vps355203:/var/www/carmelina.napolitano# git clone https://github.com/campus-digital-grenoble/code-closet.git
Cloning into 'code-closet'...
Username for 'https://github.com': anilemraC
Password for 'https://anilemraC@github.com':
remote: Counting objects: 1554, done.
remote: Compressing objects: 100% (27/27), done.
remote: Total 1554 (delta 5), reused 0 (delta 0), pack-reused 1527
Receiving objects: 100% (1554/1554), 20.52 MiB | 9.53 MiB/s, done.
Resolving deltas: 100% (1086/1086), done.
Checking connectivity... done.
root@vps355203:/var/www/carmelina.napolitano# ls
code-closet
root@vps355203:/var/www/carmelina.napolitano# cat /etc/apache2/sites-enabled/carmelina.conf
<VirtualHost *:80>
        DocumentRoot /var/www/carmelina.napolitano
        ServerName carmelina.code-closet.com
RewriteEngine on
RewriteCond %{SERVER_NAME} =carmelina.code-closet.com
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,QSA,R=permanent]
</VirtualHost>

root@vps355203:/var/www/carmelina.napolitano# cd var$
-bash: cd: var$: No such file or directory
root@vps355203:/var/www/carmelina.napolitano#
root@vps355203:/var/www/carmelina.napolitano# cd code-closet/public/
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# l
total 28
drwxr-xr-x 2 root root 4096 Jan 19 14:32 css
-rw-r--r-- 1 root root    0 Jan 19 14:32 favicon.ico
-rw-r--r-- 1 root root  553 Jan 19 14:32 .htaccess
drwxr-xr-x 2 root root 4096 Jan 19 14:32 images
-rw-r--r-- 1 root root 1782 Jan 19 14:32 index.php
drwxr-xr-x 2 root root 4096 Jan 19 14:32 js
-rw-r--r-- 1 root root   24 Jan 19 14:32 robots.txt
-rw-r--r-- 1 root root  914 Jan 19 14:32 web.config
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# ls
css  favicon.ico  images  index.php  js  robots.txt  web.config
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# pwd
/var/www/carmelina.napolitano/code-closet/public
root@vps355203:/var/www/carmelina.napolitano/code-closet/public#
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# pwd
/var/www/carmelina.napolitano/code-closet/public
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# nano /etc/apache2/sites-enabled/carmelina.conf
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# service apache2 restart
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /etc/apache2/sites-enabled/carmelina.conf
<VirtualHost *:80>
        DocumentRoot /var/www/carmelina.napolitano/code-closet/public
        ServerName carmelina.code-closet.com
RewriteEngine on
RewriteCond %{SERVER_NAME} =carmelina.code-closet.com
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,QSA,R=permanent]
</VirtualHost>

root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cd /etc/apache2/sites-enabled/
root@vps355203:/etc/apache2/sites-enabled# ls
carmelina.conf  carmelina-le-ssl.conf  code-closet.conf  germain.conf  loic.conf  loic-le-ssl.conf  loic.maupin.conf  sergio.conf  serg
root@vps355203:/etc/apache2/sites-enabled# nano carmelina-le-ssl.conf
root@vps355203:/etc/apache2/sites-enabled# cat code-closet.conf
<VirtualHost *:80>
DocumentRoot /var/www/html/code-closet/public/
ServerName code-closet.com
        <Directory /var/www/html/code-closet/public/>
                AllowOverride All
        </Directory>
</VirtualHost>
root@vps355203:/etc/apache2/sites-enabled# cat carmelina.conf
<VirtualHost *:80>
        DocumentRoot /var/www/carmelina.napolitano/code-closet/public
        ServerName carmelina.code-closet.com
RewriteEngine on
RewriteCond %{SERVER_NAME} =carmelina.code-closet.com
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,QSA,R=permanent]
</VirtualHost>

root@vps355203:/etc/apache2/sites-enabled# cat carmelina-le-ssl.conf
<IfModule mod_ssl.c>
<VirtualHost *:443>
        DocumentRoot /var/www/carmelina.napolitano
        ServerName carmelina.napolitano.campus-grenoble.fr
SSLCertificateFile /etc/letsencrypt/live/sergio.courtois.campus-grenoble.fr/fullchain.pem
SSLCertificateKeyFile /etc/letsencrypt/live/sergio.courtois.campus-grenoble.fr/privkey.pem
Include /etc/letsencrypt/options-ssl-apache.conf
</VirtualHost>
</IfModule>
root@vps355203:/etc/apache2/sites-enabled# fg
-bash: fg: current: no such job
root@vps355203:/etc/apache2/sites-enabled# nano carmelina
root@vps355203:/etc/apache2/sites-enabled# nano carmelina

[1]+  Stopped                 nano carmelina
root@vps355203:/etc/apache2/sites-enabled# fg
nano carmelina
root@vps355203:/etc/apache2/sites-enabled# nano carmelina
carmelina.conf         carmelina-le-ssl.conf
root@vps355203:/etc/apache2/sites-enabled# nano carmelina-le-ssl.conf
root@vps355203:/var/www/carmelina.napolitano/code-closet/public#

[1]+  Stopped                 nano carmelina-le-ssl.conf
root@vps355203:/etc/apache2/sites-enabled# pwd
/etc/apache2/sites-enabled
root@vps355203:/etc/apache2/sites-enabled# cd /var/www/carmelina.napolitano/
root@vps355203:/var/www/carmelina.napolitano# ls
code-closet
root@vps355203:/var/www/carmelina.napolitano# cd code-closet/public/
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# ls
css  favicon.ico  images  index.php  js  robots.txt  web.config
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# pwd
/var/www/carmelina.napolitano/code-closet/public
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# fg
nano carmelina-le-ssl.conf      (wd: /etc/apache2/sites-enabled)
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# service apache2 restart
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /var/log/apache2/
access.log                     error.log.14.gz                error.log.9.gz                 other_vhosts_access.log.2.gz
access.log.1                   error.log.2.gz                 other_vhosts_access.log        other_vhosts_access.log.3.gz
error.log                      error.log.3.gz                 other_vhosts_access.log.1      other_vhosts_access.log.4.gz
error.log.1                    error.log.4.gz                 other_vhosts_access.log.10.gz  other_vhosts_access.log.5.gz
error.log.10.gz                error.log.5.gz                 other_vhosts_access.log.11.gz  other_vhosts_access.log.6.gz
error.log.11.gz                error.log.6.gz                 other_vhosts_access.log.12.gz  other_vhosts_access.log.7.gz
error.log.12.gz                error.log.7.gz                 other_vhosts_access.log.13.gz  other_vhosts_access.log.8.gz
error.log.13.gz                error.log.8.gz                 other_vhosts_access.log.14.gz  other_vhosts_access.log.9.gz
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /var/log/apache2/
access.log                     error.log.14.gz                error.log.9.gz                 other_vhosts_access.log.2.gz
access.log.1                   error.log.2.gz                 other_vhosts_access.log        other_vhosts_access.log.3.gz
error.log                      error.log.3.gz                 other_vhosts_access.log.1      other_vhosts_access.log.4.gz
error.log.1                    error.log.4.gz                 other_vhosts_access.log.10.gz  other_vhosts_access.log.5.gz
error.log.10.gz                error.log.5.gz                 other_vhosts_access.log.11.gz  other_vhosts_access.log.6.gz
error.log.11.gz                error.log.6.gz                 other_vhosts_access.log.12.gz  other_vhosts_access.log.7.gz
error.log.12.gz                error.log.7.gz                 other_vhosts_access.log.13.gz  other_vhosts_access.log.8.gz
error.log.13.gz                error.log.8.gz                 other_vhosts_access.log.14.gz  other_vhosts_access.log.9.gz
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /var/log/apache2/
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /var/log/apache2/
access.log                     error.log.14.gz                error.log.9.gz                 other_vhosts_access.log.2.gz
access.log.1                   error.log.2.gz                 other_vhosts_access.log        other_vhosts_access.log.3.gz
error.log                      error.log.3.gz                 other_vhosts_access.log.1      other_vhosts_access.log.4.gz
error.log.1                    error.log.4.gz                 other_vhosts_access.log.10.gz  other_vhosts_access.log.5.gz
error.log.10.gz                error.log.5.gz                 other_vhosts_access.log.11.gz  other_vhosts_access.log.6.gz
error.log.11.gz                error.log.6.gz                 other_vhosts_access.log.12.gz  other_vhosts_access.log.7.gz
error.log.12.gz                error.log.7.gz                 other_vhosts_access.log.13.gz  other_vhosts_access.log.8.gz
error.log.13.gz                error.log.8.gz                 other_vhosts_access.log.14.gz  other_vhosts_access.log.9.gz
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /var/log/apache2/other_vhosts_access.log
other_vhosts_access.log        other_vhosts_access.log.12.gz  other_vhosts_access.log.3.gz   other_vhosts_access.log.7.gz
other_vhosts_access.log.1      other_vhosts_access.log.13.gz  other_vhosts_access.log.4.gz   other_vhosts_access.log.8.gz
other_vhosts_access.log.10.gz  other_vhosts_access.log.14.gz  other_vhosts_access.log.5.gz   other_vhosts_access.log.9.gz
other_vhosts_access.log.11.gz  other_vhosts_access.log.2.gz   other_vhosts_access.log.6.gz
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /var/log/apache2/
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /var/log/apache2/
access.log                     error.log.14.gz                error.log.9.gz                 other_vhosts_access.log.2.gz
access.log.1                   error.log.2.gz                 other_vhosts_access.log        other_vhosts_access.log.3.gz
error.log                      error.log.3.gz                 other_vhosts_access.log.1      other_vhosts_access.log.4.gz
error.log.1                    error.log.4.gz                 other_vhosts_access.log.10.gz  other_vhosts_access.log.5.gz
error.log.10.gz                error.log.5.gz                 other_vhosts_access.log.11.gz  other_vhosts_access.log.6.gz
error.log.11.gz                error.log.6.gz                 other_vhosts_access.log.12.gz  other_vhosts_access.log.7.gz
error.log.12.gz                error.log.7.gz                 other_vhosts_access.log.13.gz  other_vhosts_access.log.8.gz
error.log.13.gz                error.log.8.gz                 other_vhosts_access.log.14.gz  other_vhosts_access.log.9.gz
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cat /var/log/apache2/error.log
[Thu Jan 19 06:25:02.543515 2017] [mpm_prefork:notice] [pid 12502] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 06:25:02.543544 2017] [core:notice] [pid 12502] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 08:47:29.649380 2017] [:error] [pid 20874] [client 195.154.181.162:52041] script '/var/www/carmelina.napolitano/logo_img.php' not found or unable to stat, referer: http://snij.de/logo_img.php
[Thu Jan 19 10:15:14.362419 2017] [mpm_prefork:notice] [pid 12502] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 10:15:15.270493 2017] [mpm_prefork:notice] [pid 22786] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 10:15:15.270554 2017] [core:notice] [pid 22786] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 10:20:13.588630 2017] [:error] [pid 22793] [client 104.192.3.34:55181] script '/var/www/carmelina.napolitano/xmlrpc.php' not found or unable to stat
[Thu Jan 19 10:47:23.513236 2017] [mpm_prefork:notice] [pid 22786] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 10:47:24.632738 2017] [mpm_prefork:notice] [pid 23051] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 10:47:24.632806 2017] [core:notice] [pid 23051] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:00:04.061544 2017] [mpm_prefork:notice] [pid 23051] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 11:00:05.187876 2017] [mpm_prefork:notice] [pid 23155] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 11:00:05.187944 2017] [core:notice] [pid 23155] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:23:57.803828 2017] [mpm_prefork:notice] [pid 23155] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 11:23:58.691775 2017] [mpm_prefork:notice] [pid 23371] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 11:23:58.691834 2017] [core:notice] [pid 23371] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:28:18.516521 2017] [mpm_prefork:notice] [pid 23371] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 11:28:19.368815 2017] [mpm_prefork:notice] [pid 23464] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 11:28:19.368881 2017] [core:notice] [pid 23464] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:30:50.728801 2017] [mpm_prefork:notice] [pid 23464] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 11:30:51.583064 2017] [mpm_prefork:notice] [pid 23544] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 11:30:51.583111 2017] [core:notice] [pid 23544] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:31:20.341964 2017] [mpm_prefork:notice] [pid 23544] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 11:31:21.446478 2017] [mpm_prefork:notice] [pid 23628] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 11:31:21.446527 2017] [core:notice] [pid 23628] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:32:36.189963 2017] [mpm_prefork:notice] [pid 23628] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 11:32:37.313626 2017] [mpm_prefork:notice] [pid 23706] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 11:32:37.313679 2017] [core:notice] [pid 23706] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:32:41.298069 2017] [:error] [pid 23712] [client 89.227.215.1:51946] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:32:41.298118 2017] [:error] [pid 23712] [client 89.227.215.1:51946] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:32:42.889093 2017] [:error] [pid 23713] [client 89.227.215.1:51948] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:32:42.893116 2017] [:error] [pid 23713] [client 89.227.215.1:51948] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:34:16.494617 2017] [mpm_prefork:notice] [pid 23706] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 11:34:17.353594 2017] [mpm_prefork:notice] [pid 23787] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 11:34:17.353637 2017] [core:notice] [pid 23787] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:34:20.920819 2017] [:error] [pid 23793] [client 89.227.215.1:51960] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:34:20.920870 2017] [:error] [pid 23793] [client 89.227.215.1:51960] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:34:21.510413 2017] [:error] [pid 23794] [client 89.227.215.1:51961] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:34:21.514113 2017] [:error] [pid 23794] [client 89.227.215.1:51961] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:34:22.004190 2017] [:error] [pid 23795] [client 89.227.215.1:51962] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:34:22.004246 2017] [:error] [pid 23795] [client 89.227.215.1:51962] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:36:25.456875 2017] [:error] [pid 23791] [client 89.227.215.1:52183] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:36:25.456932 2017] [:error] [pid 23791] [client 89.227.215.1:52183] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:36:26.108929 2017] [:error] [pid 23794] [client 89.227.215.1:52185] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:36:26.108960 2017] [:error] [pid 23794] [client 89.227.215.1:52185] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:36:26.301826 2017] [:error] [pid 23795] [client 89.227.215.1:52187] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:36:26.301870 2017] [:error] [pid 23795] [client 89.227.215.1:52187] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:36:26.497657 2017] [:error] [pid 23793] [client 89.227.215.1:52189] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:36:26.497689 2017] [:error] [pid 23793] [client 89.227.215.1:52189] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:01.623550 2017] [:error] [pid 23794] [client 89.227.215.1:51308] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:01.623594 2017] [:error] [pid 23794] [client 89.227.215.1:51308] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:02.712795 2017] [:error] [pid 23793] [client 89.227.215.1:51311] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:02.712837 2017] [:error] [pid 23793] [client 89.227.215.1:51311] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:02.946573 2017] [:error] [pid 23795] [client 89.227.215.1:51313] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:02.946639 2017] [:error] [pid 23795] [client 89.227.215.1:51313] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:03.154153 2017] [:error] [pid 23791] [client 89.227.215.1:51315] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:03.154210 2017] [:error] [pid 23791] [client 89.227.215.1:51315] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:03.346601 2017] [:error] [pid 23794] [client 89.227.215.1:51317] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:03.346641 2017] [:error] [pid 23794] [client 89.227.215.1:51317] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:03.574610 2017] [:error] [pid 23792] [client 89.227.215.1:51319] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:03.574679 2017] [:error] [pid 23792] [client 89.227.215.1:51319] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:03.775672 2017] [:error] [pid 23793] [client 89.227.215.1:51321] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:41:03.775716 2017] [:error] [pid 23793] [client 89.227.215.1:51321] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:48:18.211688 2017] [:error] [pid 23791] [client 89.227.215.1:51328] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:48:18.211726 2017] [:error] [pid 23791] [client 89.227.215.1:51328] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:48:18.983242 2017] [:error] [pid 23792] [client 89.227.215.1:51330] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:48:18.983278 2017] [:error] [pid 23792] [client 89.227.215.1:51330] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:48:42.850499 2017] [:error] [pid 23795] [client 89.227.215.1:52297] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:48:42.850559 2017] [:error] [pid 23795] [client 89.227.215.1:52297] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:31.686025 2017] [mpm_prefork:notice] [pid 23787] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 11:50:32.798448 2017] [mpm_prefork:notice] [pid 23952] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 11:50:32.798501 2017] [core:notice] [pid 23952] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 11:50:39.158830 2017] [:error] [pid 23958] [client 89.227.215.1:51336] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:39.158877 2017] [:error] [pid 23958] [client 89.227.215.1:51336] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:39.994580 2017] [:error] [pid 23957] [client 89.227.215.1:51338] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:39.994624 2017] [:error] [pid 23957] [client 89.227.215.1:51338] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:40.242049 2017] [:error] [pid 23959] [client 89.227.215.1:51340] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:40.242090 2017] [:error] [pid 23959] [client 89.227.215.1:51340] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:40.525511 2017] [:error] [pid 23956] [client 89.227.215.1:51342] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:40.525578 2017] [:error] [pid 23956] [client 89.227.215.1:51342] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:51.762446 2017] [:error] [pid 23960] [client 89.227.215.1:51346] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:51.762534 2017] [:error] [pid 23960] [client 89.227.215.1:51346] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:51.955093 2017] [:error] [pid 23957] [client 89.227.215.1:51348] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:51.955183 2017] [:error] [pid 23957] [client 89.227.215.1:51348] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:52.253621 2017] [:error] [pid 23959] [client 89.227.215.1:51350] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:52.253674 2017] [:error] [pid 23959] [client 89.227.215.1:51350] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:52.414591 2017] [:error] [pid 23956] [client 89.227.215.1:51352] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:50:52.414655 2017] [:error] [pid 23956] [client 89.227.215.1:51352] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:35.507111 2017] [:error] [pid 23959] [client 89.227.215.1:51398] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:35.507158 2017] [:error] [pid 23959] [client 89.227.215.1:51398] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:35.787815 2017] [:error] [pid 23958] [client 89.227.215.1:51400] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:35.787845 2017] [:error] [pid 23958] [client 89.227.215.1:51400] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:35.990188 2017] [:error] [pid 23967] [client 89.227.215.1:51402] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:35.990231 2017] [:error] [pid 23967] [client 89.227.215.1:51402] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:36.261947 2017] [:error] [pid 23957] [client 89.227.215.1:51404] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:36.261984 2017] [:error] [pid 23957] [client 89.227.215.1:51404] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:36.508594 2017] [:error] [pid 23960] [client 89.227.215.1:51406] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:36.508639 2017] [:error] [pid 23960] [client 89.227.215.1:51406] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:37.107422 2017] [:error] [pid 23956] [client 89.227.215.1:51408] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:37.107466 2017] [:error] [pid 23956] [client 89.227.215.1:51408] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:37.314594 2017] [:error] [pid 23957] [client 89.227.215.1:51410] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:37.314669 2017] [:error] [pid 23957] [client 89.227.215.1:51410] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:37.530950 2017] [:error] [pid 23958] [client 89.227.215.1:51412] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:53:37.530981 2017] [:error] [pid 23958] [client 89.227.215.1:51412] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:07.135022 2017] [:error] [pid 23960] [client 89.227.215.1:51439] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:07.135169 2017] [:error] [pid 23960] [client 89.227.215.1:51439] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:07.716829 2017] [:error] [pid 23956] [client 89.227.215.1:51442] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:07.716861 2017] [:error] [pid 23956] [client 89.227.215.1:51442] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:07.875620 2017] [:error] [pid 23958] [client 89.227.215.1:51444] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:07.875670 2017] [:error] [pid 23958] [client 89.227.215.1:51444] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:08.044247 2017] [:error] [pid 23957] [client 89.227.215.1:51446] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:08.044298 2017] [:error] [pid 23957] [client 89.227.215.1:51446] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:08.205756 2017] [:error] [pid 23959] [client 89.227.215.1:51448] PHP Warning:  require(/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 11:59:08.205811 2017] [:error] [pid 23959] [client 89.227.215.1:51448] PHP Fatal error:  require(): Failed opening required '/var/www/html/sergio.courtois/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/sergio.courtois/bootstrap/autoload.php on line 17
[Thu Jan 19 13:06:26.423138 2017] [:error] [pid 23958] [client 89.227.215.1:52397] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 13:06:26.423242 2017] [:error] [pid 23958] [client 89.227.215.1:52397] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 13:08:08.348639 2017] [:error] [pid 23957] [client 89.227.215.1:52407] PHP Warning:  require(/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 13:08:08.351860 2017] [:error] [pid 23957] [client 89.227.215.1:52407] PHP Fatal error:  require(): Failed opening required '/var/www/html/loic_site/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/html/loic_site/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 13:28:25.938061 2017] [mpm_prefork:notice] [pid 23952] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 13:28:27.061595 2017] [mpm_prefork:notice] [pid 24270] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 13:28:27.061650 2017] [core:notice] [pid 24270] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 13:28:33.843061 2017] [core:alert] [pid 24276] [client 89.227.215.1:52493] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:36:24.504591 2017] [mpm_prefork:notice] [pid 24270] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 13:36:25.614069 2017] [mpm_prefork:notice] [pid 24364] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 13:36:25.614114 2017] [core:notice] [pid 24364] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 13:36:29.929415 2017] [core:alert] [pid 24370] [client 89.227.215.1:52500] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:36:30.877242 2017] [core:alert] [pid 24369] [client 89.227.215.1:52501] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:36:31.372737 2017] [core:alert] [pid 24368] [client 89.227.215.1:52503] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:36:31.772329 2017] [core:alert] [pid 24371] [client 89.227.215.1:52505] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:42:29.292571 2017] [core:alert] [pid 24369] [client 89.227.215.1:52524] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:42:30.089247 2017] [core:alert] [pid 24368] [client 89.227.215.1:52525] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:46:04.210235 2017] [core:alert] [pid 24371] [client 89.227.215.1:52539] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:49:44.904493 2017] [core:alert] [pid 24370] [client 89.227.215.1:52548] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:49:46.032288 2017] [core:alert] [pid 24369] [client 89.227.215.1:52550] /var/www/html/loic_site/code-closet/public/.htaccess: <Directory not allowed here
[Thu Jan 19 13:51:01.202134 2017] [mpm_prefork:notice] [pid 24364] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 14:13:37.655789 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:13:37.655869 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:13:43.339383 2017] [:error] [pid 24954] [client 89.227.215.1:52728] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/loic_site/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(UnexpectedValueException), Array)\n#3 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(UnexpectedValueException), Array)\n#4 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(UnexpectedValueException), Array)\n#5 /var/www/html/loic_site/code-cl in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:13:43.340116 2017] [:error] [pid 24954] [client 89.227.215.1:52728] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/loic_site/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Co in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:14:42.759322 2017] [:error] [pid 24952] [client 89.227.215.1:51569] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(ErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(ErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(ErrorException), Array)\n#5 /var/www/html/code-closet/vendor/laravel/framework/src/Illuminate/Foundation/Exceptions/Handler.php(71): Illuminate\\Log\\Writer->err in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:14:42.760993 2017] [:error] [pid 24952] [client 89.227.215.1:51569] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#5 /var/www/html/ in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:14:57.763738 2017] [mpm_prefork:notice] [pid 24948] AH00171: Graceful restart requested, doing restart
AH00112: Warning: DocumentRoot [/var/www/germain/public/code-closet/index.blade.php] does not exist
[Thu Jan 19 14:14:57.860982 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:14:57.860999 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:16:48.404880 2017] [:error] [pid 24996] [client 89.227.215.1:52746] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/loic_site/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(UnexpectedValueException), Array)\n#3 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(UnexpectedValueException), Array)\n#4 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(UnexpectedValueException), Array)\n#5 /var/www/html/loic_site/code-cl in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:16:48.405562 2017] [:error] [pid 24996] [client 89.227.215.1:52746] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/loic_site/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Co in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:17:21.501563 2017] [:error] [pid 24999] [client 89.227.215.1:52749] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/loic_site/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(UnexpectedValueException), Array)\n#3 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(UnexpectedValueException), Array)\n#4 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(UnexpectedValueException), Array)\n#5 /var/www/html/loic_site/code-cl in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:17:21.502162 2017] [:error] [pid 24999] [client 89.227.215.1:52749] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/loic_site/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Co in /var/www/html/loic_site/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:20:06.141664 2017] [:error] [pid 24995] [client 89.227.215.1:52776] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(ErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(ErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(ErrorException), Array)\n#5 /var/www/html/code-closet/vendor/laravel/framework/src/Illuminate/Foundation/Exceptions/Handler.php(71): Illuminate\\Log\\Writer->err in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:20:06.142365 2017] [:error] [pid 24995] [client 89.227.215.1:52776] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#5 /var/www/html/ in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:24:21.622355 2017] [mpm_prefork:notice] [pid 24948] AH00171: Graceful restart requested, doing restart
AH00112: Warning: DocumentRoot [/var/www/germain/public/code-closet/resources/views/pages/index.blade.php] does not exist
[Thu Jan 19 14:24:21.737637 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:24:21.737656 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:30:42.220698 2017] [:error] [pid 25150] [client 89.227.215.1:52821] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(ErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(ErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(ErrorException), Array)\n#5 /var/www/html/code-closet/vendor/laravel/framework/src/Illuminate/Foundation/Exceptions/Handler.php(71): Illuminate\\Log\\Writer->err in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157, referer: http://code-closet.com/
[Thu Jan 19 14:30:42.221424 2017] [:error] [pid 25150] [client 89.227.215.1:52821] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#5 /var/www/html/ in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157, referer: http://code-closet.com/
[Thu Jan 19 14:32:39.268774 2017] [mpm_prefork:notice] [pid 24948] AH00171: Graceful restart requested, doing restart
[Thu Jan 19 14:32:39.530837 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:32:39.530856 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:37:31.075510 2017] [mpm_prefork:notice] [pid 24948] AH00171: Graceful restart requested, doing restart
[Thu Jan 19 14:37:31.206735 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:37:31.206752 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:42:09.648079 2017] [mpm_prefork:notice] [pid 24948] AH00171: Graceful restart requested, doing restart
AH00112: Warning: DocumentRoot [/var/www/germain/public/code-closet/public/index.php] does not exist
[Thu Jan 19 14:42:09.738925 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:42:09.738941 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:42:23.638470 2017] [:error] [pid 25815] [client 89.227.215.1:49335] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17, referer: http://germain.code-closet.com/code-closet/
[Thu Jan 19 14:42:23.638499 2017] [:error] [pid 25815] [client 89.227.215.1:49335] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17, referer: http://germain.code-closet.com/code-closet/
[Thu Jan 19 14:42:27.319059 2017] [:error] [pid 25816] [client 89.227.215.1:49341] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 14:42:27.319101 2017] [:error] [pid 25816] [client 89.227.215.1:49341] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 14:42:57.301551 2017] [:error] [pid 25816] [client 89.227.215.1:49359] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(ErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(ErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(ErrorException), Array)\n#5 /var/www/html/code-closet/vendor/laravel/framework/src/Illuminate/Foundation/Exceptions/Handler.php(71): Illuminate\\Log\\Writer->err in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:42:57.302256 2017] [:error] [pid 25816] [client 89.227.215.1:49359] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#5 /var/www/html/ in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 14:47:20.697782 2017] [mpm_prefork:notice] [pid 24948] AH00171: Graceful restart requested, doing restart
AH00112: Warning: DocumentRoot [/var/www/germain/code-closet/public/index.php] does not exist
[Thu Jan 19 14:47:20.839584 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:47:20.839598 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:50:31.056912 2017] [mpm_prefork:notice] [pid 24948] AH00171: Graceful restart requested, doing restart
AH00112: Warning: DocumentRoot [/var/www/germain/code-closet/test/test.html] does not exist
[Thu Jan 19 14:50:31.158388 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:50:31.158402 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:52:45.777541 2017] [mpm_prefork:notice] [pid 24948] AH00171: Graceful restart requested, doing restart
AH00112: Warning: DocumentRoot [/var/www/germain/code-closet/test/index.html] does not exist
[Thu Jan 19 14:52:45.868749 2017] [mpm_prefork:notice] [pid 24948] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:52:45.868768 2017] [core:notice] [pid 24948] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:55:25.605324 2017] [mpm_prefork:notice] [pid 24948] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 14:55:26.722897 2017] [mpm_prefork:notice] [pid 26026] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:55:26.722947 2017] [core:notice] [pid 26026] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:56:17.786739 2017] [:error] [pid 26038] [client 89.227.215.1:52081] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17, referer: https://carmelina.code-closet.com/code-closet/
[Thu Jan 19 14:56:17.786787 2017] [:error] [pid 26038] [client 89.227.215.1:52081] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17, referer: https://carmelina.code-closet.com/code-closet/
[Thu Jan 19 14:56:21.427803 2017] [:error] [pid 26033] [client 89.227.215.1:52093] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 14:56:21.427845 2017] [:error] [pid 26033] [client 89.227.215.1:52093] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 14:57:10.697650 2017] [mpm_prefork:notice] [pid 26026] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 14:57:11.806716 2017] [mpm_prefork:notice] [pid 26104] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 14:57:11.806772 2017] [core:notice] [pid 26104] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 14:57:37.171893 2017] [:error] [pid 26122] [client 89.227.215.1:52972] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(ErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(ErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(ErrorException), Array)\n#5 /var/www/html/code-closet/vendor/laravel/framework/src/Illuminate/Foundation/Exceptions/Handler.php(71): Illuminate\\Log\\Writer->err in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157, referer: http://code-closet.com/
[Thu Jan 19 14:57:37.172674 2017] [:error] [pid 26122] [client 89.227.215.1:52972] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#5 /var/www/html/ in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157, referer: http://code-closet.com/
[Thu Jan 19 14:57:49.259671 2017] [:error] [pid 26117] [client 89.227.215.1:52989] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(ErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(ErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(ErrorException), Array)\n#5 /var/www/html/code-closet/vendor/laravel/framework/src/Illuminate/Foundation/Exceptions/Handler.php(71): Illuminate\\Log\\Writer->err in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157, referer: http://code-closet.com/accueil
[Thu Jan 19 14:57:49.260036 2017] [:error] [pid 26117] [client 89.227.215.1:52989] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#5 /var/www/html/ in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157, referer: http://code-closet.com/accueil
[Thu Jan 19 14:57:52.177696 2017] [:error] [pid 26117] [client 89.227.215.1:52989] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(ErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(ErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(ErrorException), Array)\n#5 /var/www/html/code-closet/vendor/laravel/framework/src/Illuminate/Foundation/Exceptions/Handler.php(71): Illuminate\\Log\\Writer->err in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157, referer: http://code-closet.com/
[Thu Jan 19 14:57:52.178031 2017] [:error] [pid 26117] [client 89.227.215.1:52989] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/html/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/html/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/html/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/html/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/html/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/html/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/html/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#5 /var/www/html/ in /var/www/html/code-closet/bootstrap/cache/compiled.php on line 14157, referer: http://code-closet.com/
[Thu Jan 19 15:02:57.199324 2017] [mpm_prefork:notice] [pid 26104] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 15:02:58.067518 2017] [ssl:warn] [pid 26238] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:02:58.122409 2017] [ssl:warn] [pid 26239] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:02:58.125460 2017] [mpm_prefork:notice] [pid 26239] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 15:02:58.125485 2017] [core:notice] [pid 26239] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 15:03:04.764489 2017] [:error] [pid 26243] [client 89.227.215.1:52139] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:03:04.764620 2017] [:error] [pid 26243] [client 89.227.215.1:52139] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:03:37.345629 2017] [mpm_prefork:notice] [pid 26239] AH00169: caught SIGTERM, shutting down
[Thu Jan 19 15:03:38.429643 2017] [ssl:warn] [pid 26302] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:03:38.472638 2017] [ssl:warn] [pid 26303] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:03:38.475392 2017] [mpm_prefork:notice] [pid 26303] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 15:03:38.475421 2017] [core:notice] [pid 26303] AH00094: Command line: '/usr/sbin/apache2'
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# tail -f /var/log/apache2/error.log
[Thu Jan 19 15:03:38.472638 2017] [ssl:warn] [pid 26303] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:03:38.475392 2017] [mpm_prefork:notice] [pid 26303] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 15:03:38.475421 2017] [core:notice] [pid 26303] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 15:06:24.168688 2017] [mpm_prefork:notice] [pid 26303] AH00171: Graceful restart requested, doing restart
AH00112: Warning: DocumentRoot [/var/www/germain/code-closet/test/index] does not exist
[Thu Jan 19 15:06:24.297835 2017] [ssl:warn] [pid 26303] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:06:24.298033 2017] [mpm_prefork:notice] [pid 26303] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 15:06:24.298041 2017] [core:notice] [pid 26303] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 15:06:27.381644 2017] [:error] [pid 26402] [client 89.227.215.1:49450] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:06:27.381689 2017] [:error] [pid 26402] [client 89.227.215.1:49450] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
























[Thu Jan 19 15:06:52.213289 2017] [mpm_prefork:notice] [pid 26303] AH00171: Graceful restart requested, doing restart
[Thu Jan 19 15:06:52.272297 2017] [ssl:warn] [pid 26303] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:06:52.272657 2017] [mpm_prefork:notice] [pid 26303] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 15:06:52.272724 2017] [core:notice] [pid 26303] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 15:06:54.591967 2017] [:error] [pid 26428] [client 89.227.215.1:49453] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:06:54.592452 2017] [:error] [pid 26428] [client 89.227.215.1:49453] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:06:55.279210 2017] [core:error] [pid 26303] AH00546: no record of generation 0 of exiting child 26428


















[Thu Jan 19 15:07:12.005499 2017] [:error] [pid 26434] [client 89.227.215.1:52153] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:07:12.005733 2017] [:error] [pid 26434] [client 89.227.215.1:52153] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:07:26.876090 2017] [:error] [pid 26433] [client 89.227.215.1:52159] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:07:26.876360 2017] [:error] [pid 26433] [client 89.227.215.1:52159] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:07:28.802917 2017] [mpm_prefork:notice] [pid 26303] AH00171: Graceful restart requested, doing restart
[Thu Jan 19 15:07:28.889282 2017] [ssl:warn] [pid 26303] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:07:28.889621 2017] [mpm_prefork:notice] [pid 26303] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 15:07:28.889681 2017] [core:notice] [pid 26303] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 15:07:32.974419 2017] [:error] [pid 26463] [client 89.227.215.1:49455] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:07:32.974596 2017] [:error] [pid 26463] [client 89.227.215.1:49455] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17










































[Thu Jan 19 15:07:41.583246 2017] [:error] [pid 26464] [client 89.227.215.1:52163] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:07:41.583424 2017] [:error] [pid 26464] [client 89.227.215.1:52163] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
^C
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# composer
Do not run Composer as root/super user! See https://getcomposer.org/root for details
   ______
  / ____/___  ____ ___  ____  ____  ________  _____
 / /   / __ \/ __ `__ \/ __ \/ __ \/ ___/ _ \/ ___/
/ /___/ /_/ / / / / / / /_/ / /_/ (__  )  __/ /
\____/\____/_/ /_/ /_/ .___/\____/____/\___/_/
                    /_/
Composer version 1.3.0 2016-12-24 00:47:03

Usage:
  command [options] [arguments]

Options:
  -h, --help                     Display this help message
  -q, --quiet                    Do not output any message
  -V, --version                  Display this application version
      --ansi                     Force ANSI output
      --no-ansi                  Disable ANSI output
  -n, --no-interaction           Do not ask any interactive question
      --profile                  Display timing and memory usage information
      --no-plugins               Whether to disable plugins.
  -d, --working-dir=WORKING-DIR  If specified, use the given directory as working directory.
  -v|vv|vvv, --verbose           Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug

Available commands:
  about           Short information about Composer
  archive         Create an archive of this composer package
  browse          Opens the package's repository URL or homepage in your browser.
  clear-cache     Clears composer's internal package cache.
  clearcache      Clears composer's internal package cache.
  config          Set config options
  create-project  Create new project from a package into given directory.
  depends         Shows which packages cause the given package to be installed
  diagnose        Diagnoses the system to identify common errors.
  dump-autoload   Dumps the autoloader
  dumpautoload    Dumps the autoloader
  exec            Execute a vendored binary/script
  global          Allows running commands in the global composer dir ($COMPOSER_HOME).
  help            Displays help for a command
  home            Opens the package's repository URL or homepage in your browser.
  info            Show information about packages
  init            Creates a basic composer.json file in current directory.
  install         Installs the project dependencies from the composer.lock file if present, or falls back on the composer.json.
  licenses        Show information about licenses of dependencies
  list            Lists commands
  outdated        Shows a list of installed packages that have updates available, including their latest version.
  prohibits       Shows which packages prevent the given package from being installed
  remove          Removes a package from the require or require-dev
  require         Adds required packages to your composer.json and installs them
  run-script      Run the scripts defined in composer.json.
  search          Search for packages
  self-update     Updates composer.phar to the latest version.
  selfupdate      Updates composer.phar to the latest version.
  show            Show information about packages
  status          Show a list of locally modified packages
  suggests        Show package suggestions
  update          Updates your dependencies to the latest version according to composer.json, and updates the composer.lock file.
  validate        Validates a composer.json and composer.lock
  why             Shows which packages cause the given package to be installed
  why-not         Shows which packages prevent the given package from being installed
root@vps355203:/var/www/carmelina.napolitano/code-closet/public# cd
root@vps355203:~# cd /var/www/carmelina.napolitano/code-closet/
root@vps355203:/var/www/carmelina.napolitano/code-closet# composer install
Do not run Composer as root/super user! See https://getcomposer.org/root for details
Loading composer repositories with package information
Installing dependencies (including require-dev) from lock file
Package operations: 62 installs, 0 updates, 0 removals
  - Installing nikic/php-parser (v3.0.2) Loading from cache
  - Installing classpreloader/classpreloader (3.1.0) Loading from cache
  - Installing doctrine/inflector (v1.1.0) Loading from cache
  - Installing jakub-onderka/php-console-color (0.1) Loading from cache
  - Installing symfony/polyfill-util (v1.3.0) Loading from cache
  - Installing symfony/polyfill-php56 (v1.3.0) Loading from cache
  - Installing jeremeamia/superclosure (2.3.0) Loading from cache
  - Installing league/flysystem (1.0.32) Loading from cache
  - Installing psr/log (1.0.2) Loading from cache
  - Installing monolog/monolog (1.22.0) Loading from cache
  - Installing mtdowling/cron-expression (v1.1.0) Loading from cache
  - Installing symfony/polyfill-mbstring (v1.3.0) Loading from cache
  - Installing symfony/translation (v3.1.8) Loading from cache
  - Installing nesbot/carbon (1.21.0) Loading from cache
  - Installing symfony/var-dumper (v3.1.8) Loading from cache
  - Installing symfony/debug (v3.1.8) Loading from cache
  - Installing symfony/console (v3.1.8) Loading from cache
  - Installing jakub-onderka/php-console-highlighter (v0.3.2) Loading from cache
  - Installing dnoegel/php-xdg-base-dir (0.1) Loading from cache
  - Installing psy/psysh (v0.8.0) Loading from cache
  - Installing paragonie/random_compat (v2.0.4) Loading from cache
  - Installing ramsey/uuid (3.5.2) Loading from cache
  - Installing swiftmailer/swiftmailer (v5.4.4) Loading from cache
  - Installing symfony/finder (v3.1.8) Loading from cache
  - Installing symfony/http-foundation (v3.1.8) Loading from cache
  - Installing symfony/event-dispatcher (v3.2.1) Loading from cache
  - Installing symfony/http-kernel (v3.1.8) Loading from cache
  - Installing symfony/process (v3.1.8) Loading from cache
  - Installing symfony/routing (v3.1.8) Loading from cache
  - Installing vlucas/phpdotenv (v2.4.0) Loading from cache
  - Installing fzaninotto/faker (v1.6.0) Loading from cache
  - Installing laravel/framework (v5.3.28) Loading from cache
  - Installing mmieluch/laravel-serve-custom-ini (dev-master e06b38b) Loading from cache
  - Installing hamcrest/hamcrest-php (v1.2.2) Loading from cache
  - Installing mockery/mockery (0.9.6) Loading from cache
  - Installing webmozart/assert (1.2.0) Loading from cache
  - Installing phpdocumentor/reflection-common (1.0) Loading from cache
  - Installing phpdocumentor/type-resolver (0.2.1) Loading from cache
  - Installing phpdocumentor/reflection-docblock (3.1.1) Loading from cache
  - Installing phpunit/php-token-stream (1.4.9) Loading from cache
  - Installing symfony/yaml (v3.2.1) Loading from cache
  - Installing sebastian/version (2.0.1) Loading from cache
  - Installing sebastian/resource-operations (1.0.0) Loading from cache
  - Installing sebastian/recursion-context (2.0.0) Loading from cache
  - Installing sebastian/object-enumerator (2.0.0) Loading from cache
  - Installing sebastian/global-state (1.1.1) Loading from cache
  - Installing sebastian/exporter (2.0.0) Loading from cache
  - Installing sebastian/environment (2.0.0) Loading from cache
  - Installing sebastian/diff (1.4.1) Loading from cache
  - Installing sebastian/comparator (1.2.2) Loading from cache
  - Installing phpunit/php-text-template (1.2.1) Loading from cache
  - Installing doctrine/instantiator (1.0.5) Loading from cache
  - Installing phpunit/phpunit-mock-objects (3.4.3) Loading from cache
  - Installing phpunit/php-timer (1.0.8) Loading from cache
  - Installing phpunit/php-file-iterator (1.4.2) Loading from cache
  - Installing sebastian/code-unit-reverse-lookup (1.0.0) Loading from cache
  - Installing phpunit/php-code-coverage (4.0.3) Loading from cache
  - Installing phpspec/prophecy (v1.6.2) Loading from cache
  - Installing myclabs/deep-copy (1.5.5) Loading from cache
  - Installing phpunit/phpunit (5.7.4) Loading from cache
  - Installing symfony/css-selector (v3.1.8) Loading from cache
  - Installing symfony/dom-crawler (v3.1.8) Loading from cache
league/flysystem suggests installing league/flysystem-aws-s3-v2 (Allows you to use S3 storage with AWS SDK v2)
league/flysystem suggests installing league/flysystem-aws-s3-v3 (Allows you to use S3 storage with AWS SDK v3)
league/flysystem suggests installing league/flysystem-azure (Allows you to use Windows Azure Blob storage)
league/flysystem suggests installing league/flysystem-cached-adapter (Flysystem adapter decorator for metadata caching)
league/flysystem suggests installing league/flysystem-copy (Allows you to use Copy.com storage)
league/flysystem suggests installing league/flysystem-dropbox (Allows you to use Dropbox storage)
league/flysystem suggests installing league/flysystem-eventable-filesystem (Allows you to use EventableFilesystem)
league/flysystem suggests installing league/flysystem-rackspace (Allows you to use Rackspace Cloud Files)
league/flysystem suggests installing league/flysystem-sftp (Allows you to use SFTP server storage via phpseclib)
league/flysystem suggests installing league/flysystem-webdav (Allows you to use WebDAV storage)
league/flysystem suggests installing league/flysystem-ziparchive (Allows you to use ZipArchive adapter)
monolog/monolog suggests installing aws/aws-sdk-php (Allow sending log messages to AWS services like DynamoDB)
monolog/monolog suggests installing doctrine/couchdb (Allow sending log messages to a CouchDB server)
monolog/monolog suggests installing ext-amqp (Allow sending log messages to an AMQP server (1.0+ required))
monolog/monolog suggests installing ext-mongo (Allow sending log messages to a MongoDB server)
monolog/monolog suggests installing graylog2/gelf-php (Allow sending log messages to a GrayLog2 server)
monolog/monolog suggests installing mongodb/mongodb (Allow sending log messages to a MongoDB server via PHP Driver)
monolog/monolog suggests installing php-amqplib/php-amqplib (Allow sending log messages to an AMQP server using php-amqplib)
monolog/monolog suggests installing php-console/php-console (Allow sending log messages to Google Chrome)
monolog/monolog suggests installing rollbar/rollbar (Allow sending log messages to Rollbar)
monolog/monolog suggests installing ruflin/elastica (Allow sending log messages to an Elastic Search server)
monolog/monolog suggests installing sentry/sentry (Allow sending log messages to a Sentry server)
symfony/translation suggests installing symfony/config ()
symfony/var-dumper suggests installing ext-symfony_debug ()
psy/psysh suggests installing ext-pdo-sqlite (The doc command requires SQLite to work.)
psy/psysh suggests installing hoa/console (A pure PHP readline implementation. You'll want this if your PHP install doesn't already support readline or libedit.)
paragonie/random_compat suggests installing ext-libsodium (Provides a modern crypto API that can be used to generate random bytes.)
ramsey/uuid suggests installing ext-libsodium (Provides the PECL libsodium extension for use with the SodiumRandomGenerator)
ramsey/uuid suggests installing ext-uuid (Provides the PECL UUID extension for use with the PeclUuidTimeGenerator and PeclUuidRandomGenerator)
ramsey/uuid suggests installing ircmaxell/random-lib (Provides RandomLib for use with the RandomLibAdapter)
ramsey/uuid suggests installing moontoast/math (Provides support for converting UUID to 128-bit integer (in string form).)
ramsey/uuid suggests installing ramsey/uuid-console (A console application for generating UUIDs with ramsey/uuid)
ramsey/uuid suggests installing ramsey/uuid-doctrine (Allows the use of Ramsey\Uuid\Uuid as Doctrine field type.)
symfony/event-dispatcher suggests installing symfony/dependency-injection ()
symfony/http-kernel suggests installing symfony/browser-kit ()
symfony/http-kernel suggests installing symfony/class-loader ()
symfony/http-kernel suggests installing symfony/config ()
symfony/http-kernel suggests installing symfony/dependency-injection ()
symfony/routing suggests installing doctrine/annotations (For using the annotation loader)
symfony/routing suggests installing symfony/config (For using the all-in-one router or any loader)
symfony/routing suggests installing symfony/dependency-injection (For loading routes from a service)
symfony/routing suggests installing symfony/expression-language (For using expression matching)
laravel/framework suggests installing aws/aws-sdk-php (Required to use the SQS queue driver and SES mail driver (~3.0).)
laravel/framework suggests installing doctrine/dbal (Required to rename columns and drop SQLite columns (~2.4).)
laravel/framework suggests installing guzzlehttp/guzzle (Required to use the Mailgun and Mandrill mail drivers and the ping methods on schedules (~5.3|~6.0).)
laravel/framework suggests installing league/flysystem-aws-s3-v3 (Required to use the Flysystem S3 driver (~1.0).)
laravel/framework suggests installing league/flysystem-rackspace (Required to use the Flysystem Rackspace driver (~1.0).)
laravel/framework suggests installing pda/pheanstalk (Required to use the beanstalk queue driver (~3.0).)
laravel/framework suggests installing predis/predis (Required to use the redis cache and queue drivers (~1.0).)
laravel/framework suggests installing pusher/pusher-php-server (Required to use the Pusher broadcast driver (~2.0).)
laravel/framework suggests installing symfony/psr-http-message-bridge (Required to use psr7 bridging features (0.2.*).)
sebastian/global-state suggests installing ext-uopz (*)
phpunit/php-code-coverage suggests installing ext-xdebug (>=2.4.0)
phpunit/phpunit suggests installing ext-xdebug (*)
phpunit/phpunit suggests installing phpunit/php-invoker (~1.1)
Generating autoload files
> Illuminate\Foundation\ComposerScripts::postInstall
> php artisan optimize
Generating optimized class loader
Compiling common classes
root@vps355203:/var/www/carmelina.napolitano/code-closet# cp .env.example .env
root@vps355203:/var/www/carmelina.napolitano/code-closet# php artisan key:generate
Application key [base64:NzQ/ULfNAki32Z/gSf9t6kNS4BykezU3qLDn9AA2/cM=] set successfully.
root@vps355203:/var/www/carmelina.napolitano/code-closet# tail -f /var/log/apache2/error.log
[Thu Jan 19 15:07:41.583424 2017] [:error] [pid 26464] [client 89.227.215.1:52163] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:09:49.338619 2017] [mpm_prefork:notice] [pid 26303] AH00171: Graceful restart requested, doing restart
AH00112: Warning: DocumentRoot [/var/www/germain/code-closet/test/index_html] does not exist
[Thu Jan 19 15:09:49.429224 2017] [ssl:warn] [pid 26303] AH01909: carmelina.code-closet.com:443:0 server certificate does NOT include an ID which matches the server name
[Thu Jan 19 15:09:49.429417 2017] [mpm_prefork:notice] [pid 26303] AH00163: Apache/2.4.10 (Debian) OpenSSL/1.0.1t configured -- resuming normal operations
[Thu Jan 19 15:09:49.429425 2017] [core:notice] [pid 26303] AH00094: Command line: '/usr/sbin/apache2'
[Thu Jan 19 15:09:52.519996 2017] [:error] [pid 26537] [client 89.227.215.1:49458] PHP Warning:  require(/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:09:52.520041 2017] [:error] [pid 26537] [client 89.227.215.1:49458] PHP Fatal error:  require(): Failed opening required '/var/www/carmelina.napolitano/code-closet/bootstrap/../vendor/autoload.php' (include_path='.:/usr/share/php:/usr/share/pear') in /var/www/carmelina.napolitano/code-closet/bootstrap/autoload.php on line 17
[Thu Jan 19 15:11:13.395905 2017] [:error] [pid 26536] [client 89.227.215.1:52224] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/carmelina.napolitano/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(UnexpectedValueException), Array)\n#3 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(UnexpectedValueException), Array)\n#4 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(UnexpectedValueException), in /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 15:11:13.396692 2017] [:error] [pid 26536] [client 89.227.215.1:52224] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/carmelina.napolitano/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\W in /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php on line 14157
























[Thu Jan 19 15:11:40.892913 2017] [:error] [pid 26537] [client 89.227.215.1:52228] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/carmelina.napolitano/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(UnexpectedValueException), Array)\n#3 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(UnexpectedValueException), Array)\n#4 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\Writer->writeLog('error', Object(UnexpectedValueException), in /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php on line 14157
[Thu Jan 19 15:11:40.893623 2017] [:error] [pid 26537] [client 89.227.215.1:52228] PHP Fatal error:  Uncaught exception 'UnexpectedValueException' with message 'The stream or file "/var/www/carmelina.napolitano/code-closet/storage/logs/laravel.log" could not be opened: failed to open stream: Permission denied' in /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php:14157\nStack trace:\n#0 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(14087): Monolog\\Handler\\StreamHandler->write(Array)\n#1 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13847): Monolog\\Handler\\AbstractProcessingHandler->handle(Array)\n#2 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13945): Monolog\\Logger->addRecord(400, Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#3 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13640): Monolog\\Logger->error(Object(Symfony\\Component\\Debug\\Exception\\FatalErrorException), Array)\n#4 /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php(13611): Illuminate\\Log\\W in /var/www/carmelina.napolitano/code-closet/bootstrap/cache/compiled.php on line 14157
^C
root@vps355203:/var/www/carmelina.napolitano/code-closet# /var/www/carmelina.napolitano/code-closet/
-bash: /var/www/carmelina.napolitano/code-closet/: Is a directory
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet#
root@vps355203:/var/www/carmelina.napolitano/code-closet# ls
app      bootstrap      composer.lock  database     package.json  public     resources  server.php  tests
artisan  composer.json  config         gulpfile.js  phpunit.xml   readme.md  routes     storage     vendor
root@vps355203:/var/www/carmelina.napolitano/code-closet# ls -l
total 196
drwxr-xr-x  6 root root   4096 Jan 19 14:32 app
-rwxr-xr-x  1 root root   1646 Jan 19 14:32 artisan
drwxr-xr-x  3 root root   4096 Jan 19 14:32 bootstrap
-rw-r--r--  1 root root   1507 Jan 19 14:32 composer.json
-rw-r--r--  1 root root 126588 Jan 19 14:32 composer.lock
drwxr-xr-x  2 root root   4096 Jan 19 14:32 config
drwxr-xr-x  5 root root   4096 Jan 19 14:32 database
-rw-r--r--  1 root root    558 Jan 19 14:32 gulpfile.js
-rw-r--r--  1 root root    401 Jan 19 14:32 package.json
-rw-r--r--  1 root root    930 Jan 19 14:32 phpunit.xml
drwxr-xr-x  5 root root   4096 Jan 19 14:32 public
-rw-r--r--  1 root root   2031 Jan 19 14:32 readme.md
drwxr-xr-x  5 root root   4096 Jan 19 14:32 resources
drwxr-xr-x  2 root root   4096 Jan 19 14:32 routes
-rw-r--r--  1 root root    563 Jan 19 14:32 server.php
drwxr-xr-x  5 root root   4096 Jan 19 14:32 storage
drwxr-xr-x  2 root root   4096 Jan 19 14:32 tests
drwxr-xr-x 32 root root   4096 Jan 19 15:10 vendor
root@vps355203:/var/www/carmelina.napolitano/code-closet# chown -R www-data:root storage
root@vps355203:/var/www/carmelina.napolitano/code-closet# ls -l
total 196
drwxr-xr-x  6 root     root   4096 Jan 19 14:32 app
-rwxr-xr-x  1 root     root   1646 Jan 19 14:32 artisan
drwxr-xr-x  3 root     root   4096 Jan 19 14:32 bootstrap
-rw-r--r--  1 root     root   1507 Jan 19 14:32 composer.json
-rw-r--r--  1 root     root 126588 Jan 19 14:32 composer.lock
drwxr-xr-x  2 root     root   4096 Jan 19 14:32 config
drwxr-xr-x  5 root     root   4096 Jan 19 14:32 database
-rw-r--r--  1 root     root    558 Jan 19 14:32 gulpfile.js
-rw-r--r--  1 root     root    401 Jan 19 14:32 package.json
-rw-r--r--  1 root     root    930 Jan 19 14:32 phpunit.xml
drwxr-xr-x  5 root     root   4096 Jan 19 14:32 public
-rw-r--r--  1 root     root   2031 Jan 19 14:32 readme.md
drwxr-xr-x  5 root     root   4096 Jan 19 14:32 resources
drwxr-xr-x  2 root     root   4096 Jan 19 14:32 routes
-rw-r--r--  1 root     root    563 Jan 19 14:32 server.php
drwxr-xr-x  5 www-data root   4096 Jan 19 14:32 storage
drwxr-xr-x  2 root     root   4096 Jan 19 14:32 tests
drwxr-xr-x 32 root     root   4096 Jan 19 15:10 vendor
root@vps355203:/var/www/carmelina.napolitano/code-closet# /etc/apache2
-bash: /etc/apache2: Is a directory
root@vps355203:/var/www/carmelina.napolitano/code-closet# cd /etc/apache2/
root@vps355203:/etc/apache2#

```
