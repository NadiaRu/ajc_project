AJC Project - 2021 /  NOURS_PROJECT

Objectif du projet: Le projet consiste à mettre en place une chaine d’intégration continu et de déploiement. 


Une première phase de déploiement de l’infrastructure devra être réalisée (automatisation). Puis la mise en place des outils nécessaires à la configuration de la chaine dite « devops ».
	=> Objectif Atteint.
	=> Déploiement VM Admin + création clients Azure via Ansible playbook.yml (Client/Serveur GitJen/Serveur LAMP) + connexion SSH entre les serveurs
	
Pour notre projet nous aurons donc besoin d’un server Gitlab (Azure), de serveurs LAMP (Azure), un serveur Jenkins (Azure), un Active Directory. Les VM déployées devront être customisées [shell : zsh, outils : htop, tmux, vim(+pathogène)]. Le provisionning devra être automatisé au maximum.
	=> Objectif Atteint.
	=> Déploiement custom sur les clients Azure et serveur Lamp (via Ansible + docker MariaDB).
	Apache2 test => http://52.187.192.129:80

Le cloud Azure ne servira que de ressources VM. (Pas d’utilisation outils Azure).
	=> Objectif Atteint. "Autant que faire se peut"
	=> Aucune manipulation manuelle Azure (excepté firewall et VPN ?).

Un, des premiers éléments sera de déployer un site web statique via Jekyll (MarkDown), les fichiers composant le site seront sur le serveur Gitlab, un commit du développeur déclenche la mise à jour du site web. (Utilisation de Gitlab CI/CD).
	=> Objectif 2/3
	=> Déploiement du site web statique via Jekyll réussi ainsi que les fichiers hébéergés sur le serveur GitLab.
	Jekyll (via Apache2) => http://52.187.192.129:4000
	=> Problème pipeline GitLab / Vm Azure
	GitLab => http://104.210.89.208:80
	Jenkins => http://104.210.89.208:8080

Un deuxième site lui sera composé d’une application php : MediaWiki (Ansible). Une haute disponibilité est requise.
	=> Objectif 1/2
	=> Déploiement de MediaWiki, pas de haute disponibilité.
	MediaWiki => http://52.187.192.129:8082/index.php/Accueil

Un troisième, une application web python, cette application sera sur le dépôt Gitlab. Un commit des développeurs déclenchera via Jenkins un build de l’image Docker. Il faudra ensuite déployer l’image dans Docker engine (Kubernetes why not ?). L’application python servira de serveur Web et affichera une page web par défaut.
	=> Objectif 1/2
	=> Déploiement application web python
	=> WebPy Python => http://52.187.192.129:8083

Un accès VPN sera nécessaire pour l’administration des serveurs applicatifs. La base de données du serveur MediaWiki devra être sauvegardée régulièrement. Les sites web devront utiliser le protocole HTTPS.
	=> Objectif 0/3


Contributors - Groupe 3 - https://github.com/NadiaRu/ajc_project
BETHENCOURT Lorine, LANDOUZY Remy, LECLERRE Thibaut, RUMIANTCEVA Nadezhda
