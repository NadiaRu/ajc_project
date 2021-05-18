### Infos
# Création le 14 mai 2021
# Dernière mise à jour le 18 mai 2021

### Déclaration de l'image de base
FROM debian:latest

### Installation python3 pip et changement du python par défaut
RUN apt-get update && apt-get install -y python3 && apt-get install -y python3-pip && alias python="python3"

### Installation du package django et création du dossier du projet
RUN pip3 install django && mkdir webpy

### Copie des fichiers à l'origine du site web et changement du répertoire courant
COPY webpy/ ./webpy/
WORKDIR ./webpy

### Exposition du port de sortie
EXPOSE 8000

### Lancement du serveur
CMD [ "python3", "manage.py", "runserver", "0.0.0.0:8000" ]
