Projet

Partie 1.

J' ai deployé toute la stack de mon infrastructure as code avec 1 seul fichier (docker-compos.yml), bien sur à l'aide des Dockerfile pour chaque application
J'avais comme consigne de déplyer des applications le plus légèrement possible notamment en utilisant des versions alpines de python (FROM python:3.9-alpine). 
En effet j'ai également optimisé mes fichiers Dockerfile comme cela (RUN pip install --upgrade pip && pip install --no-cache-dir -r requirements.txt)
Il m'a également fallu les rendre accessible depuis l'extérieur en configurant des ports spécifiques. Voici un exemple (docker run -d --name flask-adminlte -p 900:5000 flask-adminlte:dev) ICI LE PORT 900

Partie 2.

Dans notre cas, il nous a été demandé de déployer 7 applications dont une application statique avec de l'html, dans un environnement de développement avec docker. Tout cela en envoyant seulement une commande docker-compose up --build -d
-d permet ici de pouvoir taper des commandes avoir à faire un ControlC pour arreter sinon cela l'éxécute en continue.

Dans mon équipe, nous avons distibué les taches de sortes à ce que chacun travail dans un domaine ou il était le plus à l'aise. Enzo s'est chargé de la documentation à savoir récupérer des applications fonctionnels et mapper notre architecture. Tandis que moi,Mohamed, je me suis chargé de la partie technique en déployant les applications.

Les frameworks que nous avons utilisé ont choisi en vue de l'apsepct physique mais également des spécialités qu'ils proposent chacun indépendament de autres. Par exemple, l'application flask-adminlte qui offre énorméments de rensignements financiers utile dans la vie d'une entreprise.

