DNS déf: www.    .com  Système de traduction. Associe un nom de domaine à une adresse ip (pour ne pas entrer l'adresse ip dans la barre de navigation)

# Doc DNS

Consigne 
● Configurer le nom de domaine fraichement acheté et faites le pointer sur votre serveur
d’îlot, vous devrez de plus configurer votre serveur pour que votre site soit accessible
depuis celui-ci.

Nom de domaine: code-closet.com

Dans le compte OVH, onglet Zone DNS, puis carrés à droite DNS+ Ajouter une entrée
Créer le sous-domaine "carmelina.code-closet.com" et le faire pointer (CNAME) sur code-closet.com

 Pour configurer le serveur:
Dans bash -> connexion SSH: root@code-closet.com + mot de passe 2JCxOmxG
cd /etc/apache2/sites-available/
Puis éditer le fichier: nano carmelina.conf pour changer le nom du serveur avec ctrl o (écrire)

```
carmelina.napolitano@PC-DG-CAMPUS-22 MINGW64 ~
$ ssh root@code-closet.com
The authenticity of host 'code-closet.com (51.255.51.212)' can't be established.
ECDSA key fingerprint is SHA256:HmIFUvcdfqwPaVsAhK5qHV/4ZafhrT3lgc21PTtgzAM.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'code-closet.com' (ECDSA) to the list of known hosts.
Connection to code-closet.com closed by remote host.
Connection to code-closet.com closed.

carmelina.napolitano@PC-DG-CAMPUS-22 MINGW64 ~
$

carmelina.napolitano@PC-DG-CAMPUS-22 MINGW64 ~
$ ssh root@code-closet.com
root@code-closet.com's password:
Permission denied, please try again.
root@code-closet.com's password:
Connection to code-closet.com closed by remote host.
Connection to code-closet.com closed.

carmelina.napolitano@PC-DG-CAMPUS-22 MINGW64 ~
$ ssh root@code-closet.com
root@code-closet.com's password:
Permission denied, please try again.
root@code-closet.com's password:

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Wed Jan 18 15:27:38 2017 from 89.227.215.1
root@vps355203:~#
root@vps355203:~# cp
cp: missing file operand
Try 'cp --help' for more information.
root@vps355203:~# 'cp --help
>
>
>
>
>
> ^C
root@vps355203:~#
root@vps355203:~#
root@vps355203:~#
root@vps355203:~#
root@vps355203:~# ^C
root@vps355203:~# /etc/apache2/sites-available
-bash: /etc/apache2/sites-available: Is a directory
root@vps355203:~# cd /etc/apache2/sites-available
root@vps355203:/etc/apache2/sites-available# nano carmelina.conf
root@vps355203:/etc/apache2/sites-available#
root@vps355203:/etc/apache2/sites-available# nano carmelina.conf
root@vps355203:/etc/apache2/sites-available# service apache2 restart
root@vps355203:/etc/apache2/sites-available# nano carmelina.conf
root@vps355203:/etc/apache2/sites-available#

```




```
<VirtualHost *:80>
        DocumentRoot /var/www/carmelina.napolitano
        ServerName carmelina.code-closet.com
RewriteEngine on
RewriteCond %{SERVER_NAME} =carmelina.code-closet.com
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,QSA,R=permanent]
</VirtualHost>

```
