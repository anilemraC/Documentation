Cordova est un plugin open-source qui fournit une interface JavaScript entre le smartphone et l'application. 
Cela permet à l'application d'utiliser les capacités du périphérique natif au-delà de ce qui existe pour 
les applications web (capteurs, données, état du réseau).

Une application Cordova a une architecture à plusieurs éléments.
Schéma: https://cordova.apache.org/static/img/guide/cordovaapparchitecture.png

- WebView fournit à l'application son interface utilisateur entière.
- Web App, c'est là que se trouve le code de l'appli dans un fichier local index.html (CSS, JS, images...)
Il y a ici un dossier très important: config.xml, qui donne des informations sur l'application et ses paramètres
de fonctionnement.
- Les Plugins sont l'interface pour communiquer avec les composants natifs et les API du périphérique (code
natif à partir de Javascript). Ce noyau de Plugins permettent à l'application d'accéder aux capacités du 
téléphone (batterie, appareil photo, contacts...).

Cordova fournit deux workflow de base pour la création d'une application mobile:
- Cross-platform (CLI) workflow, pour une apllication qui doit fonctionner sur tout type de système 
d'exploitation mobiles.
- Platform-centered workflow, pour une application qui associe les composants natifs aux composants de 
Cordova basés sur le web.
