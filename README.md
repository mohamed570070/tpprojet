
# Projet

## Partie 1 : Déploiement de l'infrastructure

J'ai déployé toute la stack de mon infrastructure as code avec **un seul fichier** (`docker-compose.yml`), bien sûr, à l'aide des **Dockerfile** pour chaque application.  
La consigne était de déployer des applications le plus léger possible, notamment en utilisant des versions **Alpine** de Python (par exemple : `FROM python:3.9-alpine`).

J'ai également optimisé mes fichiers **Dockerfile** de cette manière :
```dockerfile
RUN pip install --upgrade pip && pip install --no-cache-dir -r requirements.txt
```

De plus, il m'a fallu rendre les applications accessibles depuis l'extérieur en configurant des ports spécifiques. Par exemple :
```bash
docker run -d --name flask-adminlte -p 900:5000 flask-adminlte:dev
```
*Ici, le port 900 est exposé*.

## Partie 2 : Déploiement des applications avec Docker

Dans notre projet, il nous a été demandé de déployer **7 applications**, dont une application statique avec du **HTML**, dans un environnement de développement avec **Docker**. Pour ce faire, une seule commande suffit :
```bash
docker-compose up --build -d
```

L'option `-d` permet de lancer les conteneurs en arrière-plan sans avoir à maintenir le terminal ouvert (vous pouvez toujours taper des commandes sans interruption).

### Répartition des tâches

Dans mon équipe, nous avons distribué les tâches de manière à ce que chacun travaille dans un domaine où il était le plus à l'aise.  
- **Enzo** s'est chargé de la documentation, c'est-à-dire récupérer des applications fonctionnelles et mapper notre architecture.  
- **Moi, Mohamed**, je me suis chargé de la partie technique en déployant les applications.

### Choix des frameworks

Les frameworks choisis ont été sélectionnés en fonction de leur aspect physique et des spécialisations qu'ils offrent indépendamment des autres. Par exemple, l'application **flask-adminlte**, qui propose une multitude d'informations financières utiles dans la gestion d'une entreprise.

## Partie 3 : Le DevOps

### Qu'est-ce que le DevOps ?

Le **DevOps** est une approche qui facilite la collaboration entre les équipes de **développement** et d'**opérations**. Dans mon projet, je me concentre principalement sur la partie **opérationnelle**, en particulier avec **Docker**. J'utilise Docker pour automatiser le déploiement et la gestion des conteneurs, ce qui garantit la cohérence des environnements et simplifie le processus de mise en production.

### En quoi le DevOps m'a-t-il aidé dans cette mission ?

Le DevOps m'a grandement facilité cette mission en automatisant et simplifiant le processus de déploiement des applications. Grâce à **Docker**, j'ai pu gérer facilement les conteneurs, en ajustant simplement les ports et les noms des applications pour les adapter à mon environnement.  
Cependant, sans le code des développeurs, je n'aurais pas pu déployer ces applications, car le code source est essentiel pour faire fonctionner les conteneurs.

### Comparaison Docker vs Machines Virtuelles

Votre chef de projet vous demande de comparer l'utilisation de **Docker** avec des **machines virtuelles** (VM).

- **Docker** est **plus léger** et **plus rapide** que les machines virtuelles, car il utilise moins de ressources en partageant le noyau du système hôte, tandis qu'une VM nécessite un système d'exploitation complet.
- **Docker** est également **plus portable**, facilitant le déploiement dans différents environnements.  
- En revanche, les **VMs** offrent une **isolement complet** du système, tandis que **Docker** s'isole uniquement au niveau de l'application.

### Outils similaires à Docker

À ma connaissance, **Kubernetes** est un autre outil similaire à Docker. Il s'agit d'un orchestrateur de conteneurs qui permet de gérer, déployer et scaler des applications conteneurisées à grande échelle, contrairement à Docker qui est plus axé sur le déploiement individuel de conteneurs.

---


# Mon projet avec plusieurs images

## Partie 1 : Déploiement de l'infrastructure



