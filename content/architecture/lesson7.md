---
title: "Session 7 : Conteneurisation et docker"
date: 2022-12-29T10:00:16+01:00
draft: false
---


# Introduction à la conteneurisation:

## Qu'est ce qu'un conteneur ?

Un conteneur est un environnement logiciel qui permet de lancer et exécuter des applications de manière isolée et autonome. Il encapsule les applications, leurs dépendances et leur configuration dans un environnement qui peut être facilement déplacé d'un système à un autre. Les conteneurs sont similaires aux machines virtuelles, mais contrairement à ces dernières, ils ne nécessitent pas de système d'exploitation virtuel, ils partagent donc le système d'exploitation hôte, ce qui les rend plus légers et plus rapides à démarrer.

Les conteneurs sont de plus en plus populaires dans l'industrie car ils permettent une meilleure portabilité, une meilleure isolation, une meilleure scalabilité et une meilleure sécurité des applications. Les développeurs peuvent facilement créer, déployer et gérer des applications en utilisant des conteneurs, ce qui permet une amélioration de la qualité et de la fiabilité des applications. Les outils de conteneurisation tels que Docker ou Kubernetes facilitent la gestion des conteneurs et peuvent être utilisés pour automatiser les tâches de déploiement, de scalabilité et de gestion des instances.

## La conteneurisation :

La conteneurisation offre plusieurs avantages par rapport aux méthodes de déploiement traditionnelles. Tout d'abord, elle permet de réduire le gaspillage de ressources en encapsulant les applications et leurs dépendances dans des conteneurs légers. Les conteneurs peuvent être déployés rapidement et facilement sur différentes plateformes, ce qui permet aux développeurs de créer des applications portables.

Elle  est une technique de virtualisation légère qui permet d'isoler les applications et leurs dépendances dans des environnements autonomes appelés conteneurs. Cette isolation permet de garantir que l'application fonctionne de manière identique sur tous les environnements, qu'il s'agisse d'un environnement de développement, de test ou de production.

## Les défis de l'environnement d'exécution des applications

Avant la conteneurisation, les applications étaient souvent déployées sur des serveurs physiques ou des machines virtuelles, ce qui présentait certains défis. Par exemple, les serveurs physiques pouvaient être surdimensionnés ou sous-dimensionnés pour les applications, ce qui entraînait un gaspillage de ressources. Les machines virtuelles étaient souvent plus légères que les serveurs physiques, mais nécessitaient tout de même une infrastructure sous-jacente.



## Les avantages de la conteneurisation incluent :

La conteneurisation offre plusieurs avantages par rapport aux méthodes de déploiement traditionnelles. Tout d'abord, elle permet de réduire le gaspillage de ressources en encapsulant les applications et leurs dépendances dans des conteneurs légers. Les conteneurs peuvent être déployés rapidement et facilement sur différentes plateformes, ce qui permet aux développeurs de créer des applications portables.


* La portabilité : Les conteneurs peuvent être déplacés facilement d'un environnement à l'autre, ce qui facilite les déploiements et les mises à jour.

* L'isolation : Les conteneurs isolent les applications les unes des autres, ce qui permet de gérer les différentes parties de l'application de manière plus efficace.

* La scalabilité : Les conteneurs peuvent être facilement dupliqués pour gérer les charges élevées, ce qui facilite la mise à l'échelle de l'application.

* La sécurité : Les conteneurs isolent les applications les unes des autres, ce qui permet de limiter les risques de sécurité.

Comparaison avec les machines virtuelles :

La conteneurisation est souvent comparée aux machines virtuelles. Les machines virtuelles créent des environnements isolés en utilisant des systèmes d'exploitation virtuels, tandis que les conteneurs partagent le même système d'exploitation hôte. Les machines virtuelles ont besoin de plus de ressources que les conteneurs et peuvent être plus lents à démarrer. Les conteneurs sont plus légers et plus rapides, ils sont donc plus adaptés pour les applications qui nécessitent une scalabilité et une flexibilité élevées.

En résumé, la conteneurisation est une technique de virtualisation légère qui permet d'isoler les applications et leurs dépendances dans des environnements autonomes appelés conteneurs. Cela permet de garantir que l'application fonctionne de manière identique sur tous les environnements, qu'il s'agisse d'un environnement de développement, de test ou de production. Il offre des avantages tels que la portabilité, l'isolation, la scalabilité et la sécurité. Il est souvent comparé aux machines virtuelles qui ont besoin de plus de ressources et peuvent être plus lents à démarrer, tandis que les conteneurs sont plus légers et plus rapides, ils sont donc plus adaptés pour les applications qui nécessitent une scalabilité et une flexibilité élevées.


## Les concepts clés de la conteneurisation : images, conteneurs, registres

La conteneurisation repose sur trois concepts clés : les images, les conteneurs et les registres.

* Une image est un package qui contient une application et toutes ses dépendances, ainsi que les instructions nécessaires pour créer un conteneur à partir de l'image.
* Un conteneur est une instance en cours d'exécution d'une image. Les conteneurs sont légers et portables, et peuvent être déployés rapidement et facilement.
* Un registre est un dépôt centralisé pour stocker et distribuer des images Docker. Le registre public de Docker, Docker Hub, contient des milliers d'images pré-construites que les développeurs peuvent utiliser pour créer des conteneurs.

# Introduction à Docker :

Docker est la technologie de conteneurisation la plus populaire et la plus largement utilisée.

### Histoire de Docker

Docker a été créé en 2013 par Solomon Hykes et est rapidement devenu un outil incontournable dans l'écosystème des applications web. La popularité de Docker est due en partie à sa facilité d'utilisation et à sa portabilité.

### Les composants de Docker : moteur Docker, CLI, Docker Hub

Docker est composé de trois éléments clés :

- Le moteur Docker : le moteur Docker est responsable de la création et de la gestion des conteneurs Docker. Il utilise l'API Docker pour communiquer avec le système d'exploitation hôte et gérer les ressources du système.
- Le Docker CLI : le Docker CLI est l'interface de ligne de commande utilisée pour communiquer avec le moteur Docker. Il permet de créer, de gérer et de déployer des conteneurs Docker à partir de la ligne de commande.
- Docker Hub : Docker Hub est un registre centralisé pour stocker et distribuer des images Docker. Il contient des milliers d'images pré-construites que les développeurs peuvent utiliser pour créer des conteneurs.

### Les avantages de Docker

Docker offre plusieurs avantages par rapport aux méthodes de déploiement traditionnelles. Tout d'abord, il permet de créer des conteneurs légers et portables qui peuvent être déployés rapidement et facilement sur différentes plateformes. De plus, Docker permet d'isoler les applications et leurs dépendances, ce qui facilite la gestion et le déploiement des applications. Enfin, Docker offre une grande flexibilité et facilite le travail en équipe en permettant aux développeurs de travailler sur des applications de manière indépendante et de partager leurs images et leurs conteneurs avec d'autres développeurs.

# Travailler avec des conteneurs Docker

Une fois que vous avez une compréhension de base de Docker, vous pouvez commencer à travailler avec des conteneurs Docker. Cette section explique comment créer des images Docker et exécuter des conteneurs.

Attention vous allez avoir besoin d'installer docker sur votre machine pour faire les commandes de cette partie du cours. 

### Créer une image Docker

Pour créer une image Docker, vous devez écrire un Dockerfile, qui est un fichier texte qui contient toutes les instructions pour créer une image. Par exemple, le Dockerfile suivant crée une image qui exécute une application web Python :

```dockerfile
FROM python:3.8-slim-buster
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
CMD ["python", "app.py"]
```


Ce Dockerfile commence par spécifier une image de base, dans ce cas python:3.8-slim-buster. Ensuite, il définit le répertoire de travail pour l'image, copie le fichier requirements.txt et installe les dépendances avec pip. Enfin, il copie le reste du code de l'application et définit la commande pour exécuter l'application.

Une fois que vous avez écrit le Dockerfile, vous pouvez créer l'image avec la commande `docker build`. Par exemple :

```sh
$ docker build -t myimage:1.0 .

```

Cette commande crée une image avec le tag `myimage:1.0` à partir du Dockerfile situé dans le répertoire courant (`.`).

### Exécuter un conteneur Docker

Une fois que vous avez créé une image Docker, vous pouvez l'exécuter en tant que conteneur avec la commande `docker run`. Par exemple :

```sh
$ docker run -p 5000:5000 myimage:1.0

```


Cette commande exécute un conteneur à partir de l'image `myimage:1.0` et mappe le port 5000 du conteneur sur le port 5000 de l'hôte.

### Configuration de l'environnement d'un conteneur Docker

Vous pouvez configurer l'environnement d'un conteneur Docker en utilisant les variables d'environnement ou les fichiers de configuration. Par exemple, vous pouvez définir une variable d'environnement dans un Dockerfile :

ENV MY_VAR=myvalue


Vous pouvez également spécifier des variables d'environnement au moment de l'exécution du conteneur avec la commande `docker run`. Par exemple :

docker run -e MY_VAR=myvalue myimage:1.0



Cette commande exécute un conteneur à partir de l'image `myimage:1.0` et définit la variable d'environnement `MY_VAR` à `myvalue`.

### Travailler avec des volumes Docker

Les volumes Docker sont utilisés pour stocker des données persistantes en dehors du conteneur. Par exemple, vous pouvez utiliser un volume Docker pour stocker des données de base de données ou des fichiers de configuration.

Pour créer un volume Docker, vous pouvez utiliser la commande `docker volume create`. Par exemple :

 docker volume create myvolume


Cette commande crée un volume Docker appelé `myvolume`.

Pour monter un volume Docker dans un conteneur, vous pouvez utiliser la commande `docker run` avec l'option `-v`. Par exemple :

 docker run -v myvolume:/data myimage:1.0



Cette commande monte le volume Docker `myvolume` dans le conteneur et le rend accessible dans le répertoire `/data`.

### Travailler avec des réseaux Docker

Les réseaux Docker permettent aux conteneurs de communiquer entre eux et avec le monde extérieur. Vous pouvez créer des réseaux Docker pour isoler vos applications et les protéger contre les attaques.

Pour créer un réseau Docker, vous pouvez utiliser la commande `docker network create`. Par exemple :

 docker network create mynetwork


Cette commande crée un réseau Docker appelé `mynetwork`.

Pour exécuter un conteneur Docker sur un réseau spécifique, vous pouvez utiliser l'option `--network` avec la commande `docker run`. Par exemple :

 docker run --network mynetwork myimage:1.0


Cette commande exécute un conteneur à partir de l'image `myimage:1.0` sur le réseau `mynetwork`.


# Les avantages de Docker dans l'industrie

La conteneurisation avec Docker est devenue très populaire dans l'industrie, car elle offre de nombreux avantages pour les entreprises et les équipes de développement.

### Déploiement facile et rapide

Avec Docker, il est facile de déployer des applications sur différentes plateformes, en utilisant les mêmes images Docker sur chaque plateforme. Les images Docker sont portables, ce qui signifie qu'elles peuvent être exécutées sur différents systèmes d'exploitation et architectures matérielles sans nécessiter de modifications.

### Isolation des applications

La conteneurisation permet d'isoler les applications et leurs dépendances, ce qui facilite la gestion des applications et réduit les conflits de dépendances. Les conteneurs sont également plus légers que les machines virtuelles, ce qui signifie qu'ils ont besoin de moins de ressources pour fonctionner.

### Flexibilité

Docker offre une grande flexibilité en permettant aux développeurs de travailler sur des applications de manière indépendante et de partager leurs images et leurs conteneurs avec d'autres développeurs. Cela facilite le travail en équipe et accélère le processus de développement.

### Maintenance des applications

Docker facilite la maintenance des applications en permettant aux développeurs de mettre à jour les images Docker et de déployer rapidement de nouvelles versions. Les conteneurs Docker peuvent être facilement arrêtés, supprimés et remplacés, ce qui facilite la gestion des mises à jour et des correctifs.

## Limites et alternatives à Docker

Bien que Docker soit devenu très populaire dans l'industrie, il existe certaines limites à cette technologie.

### Limites de Docker

- Docker peut être plus difficile à mettre en place que d'autres technologies de virtualisation, en particulier pour les utilisateurs débutants.
- Les conteneurs Docker partagent le même noyau de système d'exploitation, ce qui peut créer des problèmes de sécurité si le noyau est compromis.
- Les conteneurs Docker peuvent être moins isolés que les machines virtuelles, ce qui peut causer des problèmes de performance ou de sécurité dans certaines situations.

# Playground 

Pour la suite et les exercices de ce cours vous devez effectuer le cours docker 101 : https://www.docker.com/101-tutorial/


# QCM :

1. Docker est une technologie de virtualisation qui crée des machines virtuelles.
a. Vrai
b. Faux
c. Ni vrai ni faux
d. Peut-être

Réponse: b

2. Les conteneurs partagent le système d'exploitation hôte avec les autres conteneurs. 
a. Vrai
b. Faux
c. Ni vrai ni faux
d. Peut-être

Réponse: a

3. La conteneurisation permet de créer des applications autonomes qui incluent toutes leurs dépendances et configurations. 
a. Vrai
b. Faux
c. Ni vrai ni faux
d. La réponse D

Réponse: a

4. Quel est le registre centralisé pour stocker et distribuer des images Docker ?
a. Docker Hub
b. Docker Repository
c. Docker Store
d. Docker Image

Réponse: a

5. Les conteneurs peuvent être déployés rapidement et facilement sur différentes plateformes, ce qui permet aux développeurs de créer des applications portables.
a. Vrai
b. Faux
c. Ni vrai ni faux
d. Peut-être

Réponse: a

6. Docker est composé de trois éléments clés, lesquels ?
a. Le moteur Docker, le Docker CLI, Docker Machine
b. Le moteur Docker, le Docker Hub, Docker Container
c. Le moteur Docker, le Docker CLI, Docker Hub
d. Le moteur Docker, Docker Repository, Docker Hub

Réponse: c

7. Un conteneur est une instance en cours d'exécution de quoi ?
a. Un noyau virtuel
b. Un système d'exploitation virtuel
c. Une image Docker
d. Une machine virtuelle

Réponse: c

8. Les avantages de Docker incluent la flexibilité. Qu'est-ce que cela signifie ?
a. Docker permet aux développeurs de travailler sur des applications de manière indépendante et de partager leurs images et leurs conteneurs avec d'autres développeurs.
b. Docker permet de réduire le gaspillage de ressources en encapsulant les applications et leurs dépendances dans des conteneurs légers.
c. Docker permet de dupliquer facilement les conteneurs pour gérer les charges élevées, ce qui facilite la mise à l'échelle de l'application.
d. Docker permet de limiter les risques de sécurité en isolant les applications les unes des autres.

Réponse: a

9. Qu'est-ce que Docker Hub ?
a. Un dépôt centralisé pour stocker et distribuer des images Docker.
b. Un outil de conteneurisation utilisé pour automatiser les tâches de déploiement, de scalabilité et de gestion des instances.
c. Un service de stockage dans le cloud.
d. Un environnement de développement intégré pour les applications web.

Réponse: a

10. Comment peut-on configurer l'environnement d'un conteneur Docker ?
a. En utilisant les variables d'environnement ou les fichiers de configuration.
b. En utilisant les images Docker.
c. En utilisant les registres Docker.
d. En utilisant les conteneurs Docker.

Réponse: a