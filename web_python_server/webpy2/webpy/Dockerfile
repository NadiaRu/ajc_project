### Infos
# Création le 14 mai 2021
# Dernière mise à jour le 17 mai 2021

### Déclaration de l'image de base
FROM python:3

### Installation des packages python essentiels
#RUN alias python="python3" && apt-get -y install python3-pip
RUN pip3 install django #&& pip3 install markdown

### Copie des fichiers à l'origine du site web et changement du répertoire courant
COPY webpy/ .
WORKDIR webpy/
#RUN mkdir -p templates/nours_project/

### Création du dossier permettant le partage des logs


### Exposition des ports de sorties
EXPOSE 8000

### Lancement du serveur
CMD [ "bash", "python3 manage.py runserver 192.168.16.138:8000" ]
