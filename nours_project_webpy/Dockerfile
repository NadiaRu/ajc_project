### Infos
# Création le 14 mai 2021
# Dernière mise à jour le 17 mai 2021

### Déclaration de l'image de base
FROM python:3

### Installation des packages python essentiels
RUN pip3 install django #&& pip3 install markdown

### Copie des fichiers à l'origine du site web et changement du répertoire courant
COPY nours_project_webpy/ .
WORKDIR nours_project-webpy/

### Création du dossier permettant le partage des logs


### Exposition des ports de sorties
EXPOSE 8000

### Lancement du serveur
CMD [ "bash", "python manage.py runserver 0.0.0.0:8000" ]
