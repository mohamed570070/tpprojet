Projet

Partie 1.

J' ai deployé toute la stack de mon infrastructure as code avec 1 seul fichier (docker-compos.yml), bien sur à l'aide des Dockerfile pour chaque application
J'avais comme consigne de déplyer des applications le plus légèrement possible notamment en utilisant des versions alpines de python (FROM python:3.9-alpine). En effet j'ai également optimisé mes fichiers Dockerfile comme cela (RUN pip install --upgrade pip && pip install --no-cache-dir -r requirements.txt)
Il m'a également fallu les rendre accessible depuis l'extérieur en configurant des ports spécifiques. Voici un exemple (docker run -d --name flask-adminlte -p 900:5000 flask-adminlte:dev) ICI LE PORT 900

Partie 2.


