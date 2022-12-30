---
title: "Session 1 : Introduction à l'architecture web"
date: 2022-12-29T10:00:16+01:00
draft: false
---

# Qu'est-ce que l'architecture web ?

L'architecture web désigne la manière dont les différents éléments d'une application web (services, bases de données, front-end, etc.) sont organisés et interagissent entre eux. Elle détermine la façon dont l'application web sera conçue, développée, déployée et maintenue.


# Differentes architectures :
Il existe plusieurs types d'architecture web, qui varient selon la manière dont les différents éléments de l'application sont séparés et communiquent entre eux. Voici quelques exemples :

- **Architecture monolithe** : tous les éléments de l'application sont regroupés dans un seul et même codebase et sont déployés ensemble. Cette architecture est simple à mettre en place mais peut être difficile à évoluer et à maintenir à mesure que l'application grandit.

- **Architecture microservices** : chaque élément de l'application est développé sous forme de microservice indépendant, qui expose des interfaces de communication bien définies aux autres microservices. Cette architecture permet une grande flexibilité et une meilleure scalabilité, mais peut être plus complexe à mettre en œuvre et à maintenir du fait de la nécessité de gérer un grand nombre de microservices.

- **Architecture Serverless** : les microservices sont exécutés sur une plateforme en tant que fonctions sans serveur, qui sont déclenchées par des événements et facturées à l'utilisation. Cette architecture permet une très grande scalabilité et une faible latence, mais peut être coûteuse à mesure que l'application grandit.

Il n'y a pas de type d'architecture web qui convient à tous les cas d'utilisation, et le choix de l'architecture dépend de nombreux facteurs tels que la taille de l'application, les contraintes de temps et de budget, les exigences en matière de performances et de disponibilité, etc.

## Architecture monolithe:

L'architecture monolithe est une approche de développement d'application web qui consiste à regrouper tous les éléments de l'application dans un seul et même codebase et à les déployer ensemble. Elle est souvent utilisée pour les applications de petite et moyenne taille, qui n'ont pas besoin de scalabilité ou de flexibilité élevées.

### Avantages de l'architecture monolithe

L'architecture monolithe présente plusieurs avantages, qui en font une solution intéressante pour certaines applications :

- **Simplicité de mise en œuvre et de déploiement** : l'architecture monolithe est très simple à mettre en place et à déployer, car elle ne nécessite pas de gérer de nombreux microservices ou fonctions indépendants. Il suffit de développer l'application dans un seul codebase et de la déployer en une seule fois sur un serveur ou une plateforme de cloud.

- **Facilité de développement et de maintenance** : dans l'architecture monolithe, tous les éléments de l'application sont regroupés dans le même codebase, ce qui rend le développement et la maintenance plus faciles. Les développeurs peuvent travailler sur tous les aspects de l'application en même temps et utiliser les mêmes outils de développement et de versionning.

- **Coûts de développement et de maintenance réduits** : l'architecture monolithe permet de réduire les coûts de développement et de maintenance, car elle ne nécessite pas de gérer de nombreux microservices ou fonctions indépendantes. Elle est donc particulièrement adaptée aux petites et moyennes applications qui n'ont pas besoin de scalabilité ou de flexibilité élevées.

### Inconvénients de l'architecture monolithe

L'architecture monolithe présente cependant aussi plusieurs inconvénients, qui peuvent rendre son utilisation moins adaptée à certaines applications :

- **Manque de scalabilité et de flexibilité** : l'architecture monolithe ne permet pas de scaler facilement les différents éléments de l'application de manière indépendante. Si une partie de l'application devient très populaire et nécessite plus de ressources, il faut déployer une nouvelle version de l'application entière, ce qui peut être coûteux et prendre du temps. De même, il est difficile de mettre à jour ou de remplacer une partie de l'application sans affecter l'ensemble de l'application.

- **Complexité croissante à mesure que l'application grandit** : l'architecture monolithe peut devenir de plus en plus complexe à mesure que l'application grandit et qu'elle inclut de nouvelles fonctionnalités. Il peut être difficile de maintenir une vue d'ensemble de l'application et de la développer de manière cohérente, ce qui peut entraîner des problèmes de qualité et de performance.

- **Difficulté à gérer les dépendances entre les éléments de l'application** : dans l'architecture monolithe, il est difficile de gérer les dépendances entre les différents éléments de l'application, ce qui peut entraîner des problèmes de développement et de maintenance.

Il est important de prendre en compte ces avantages et inconvénients lors du choix de l'architecture monolithe, en fonction des besoins de l'application et de son évolution prévue.

### Exemples d'applications web monolithes

Voici quelques exemples d'applications web qui peuvent être développées selon une architecture monolithe :

- Un site de e-commerce de petite et moyenne taille, qui propose une gamme limitée de produits et qui n'a pas besoin de scalabilité élevée.
- Un site de blog ou de journal en ligne, qui affiche du contenu statique et qui n'a pas besoin de fonctionnalités de mise à jour en temps réel.
- Un site de gestion de projet pour une équipe restreinte, qui ne nécessite pas de scalabilité élevée ni de flexibilité.

### Conclusion

L'architecture monolithe est une approche de développement d'application web simple et adaptée aux applications de petite et moyenne taille qui n'ont pas besoin de scalabilité ou de flexibilité élevées. Elle présente des avantages en termes de simplicité de mise en œuvre et de déploiement, de facilité de développement et de maintenance, et de coûts réduits. Cependant, elle peut être moins adaptée aux applications qui ont besoin de scalabilité ou de flexibilité élevées, ou qui sont amenées à grandir de manière importante, car elle peut devenir complexe et difficile à maintenir dans ces cas.

## L'architecture microservices

L'architecture microservices est une approche de développement d'application web qui consiste à regrouper les éléments de l'application en plusieurs microservices indépendants, qui communiquent entre eux pour réaliser les fonctionnalités de l'application. Cette approche est souvent utilisée pour les applications de grande taille ou à forte croissance, qui ont besoin de scalabilité et de flexibilité élevées.

### Avantages de l'architecture microservices

L'architecture microservices présente plusieurs avantages, qui en font une solution intéressante pour certaines applications :

- **Scalabilité et flexibilité élevées** : dans l'architecture microservices, chaque microservice est indépendant et peut être déployé et évolué de manière indépendante. Cela permet de scaler facilement les différents éléments de l'application de manière indépendante et de mettre à jour ou de remplacer une partie de l'application sans affecter l'ensemble de l'application.

- **Facilité de développement et de maintenance** : dans l'architecture microservices, chaque microservice est développé et maintenu par une équipe dédiée, ce qui rend le développement et la maintenance plus faciles. Les développeurs peuvent travailler sur un microservice en particulier et utiliser les outils de développement et de versionning qui leur conviennent le mieux.

- **Meilleure gestion des dépendances entre les éléments de l'application** : dans l'architecture microservices, chaque microservice est indépendant et n'a pas de dépendances fortes avec les autres microservices. Cela permet de mieux gérer les dépendances entre les différents éléments de l'application et de limiter les problèmes de développement et de maintenance.

### Inconvénients de l'architecture microservices

L'architecture microservices présente cependant aussi plusieurs inconvénients, qui peuvent rendre son utilisation moins adaptée à certaines applications :

- **Coûts de développement et de maintenance élevés** : l'architecture microservices nécessite de gérer de nombreux microservices indépendants, ce qui peut augmenter les coûts de développement et de maintenance. Il faut également prévoir des outils de gestion de microservices, comme un registry ou un service mesh, ce qui peut ajouter des coûts supplémentaires.

- **Complexité croissante à mesure que l'application grandit** : l'architecture microservices peut devenir de plus en plus complexe à mesure que l'application grandit et qu'elle inclut de nouveaux microservices. Il peut être difficile de maintenir une vue d'ensemble de l'ensemble des microservices et de leurs interactions, ce qui peut entraîner des problèmes de qualité et de performance.

- **Difficulté à gérer les erreurs et les pannes** : dans l'architecture microservices, il est difficile de gérer les erreurs et les pannes, car chaque microservice est indépendant et peut être impacté par des problèmes de disponibilité ou de performance. Il faut mettre en place des outils de monitoring et de gestion des erreurs pour surveiller l'état des microservices et intervenir rapidement en cas de problème.

### Exemples d'applications web microservices

Voici quelques exemples d'applications web qui peuvent être développées selon une architecture microservices :

- Un site de e-commerce de grande taille, qui propose une large gamme de produits et qui a besoin de scalabilité élevée pour gérer de nombreux utilisateurs et commandes.
- Un site de médias en ligne, qui affiche du contenu dynamique et qui a besoin de fonctionnalités de mise à jour en temps réel.
- Un site de gestion de projet pour une équipe de grande taille, qui nécessite une flexibilité élevée et la possibilité de développer et de mettre à jour rapidement les différentes fonctionnalités.

### Conclusion

L'architecture microservices est une approche de développement d'application web adaptée aux applications de grande taille ou à forte croissance qui ont besoin de scalabilité et de flexibilité élevées. Elle présente des avantages en termes de scalabilité, de flexibilité, de facilité de développement et de maintenance, et de meilleure gestion des dépendances. Cependant, elle peut être moins adaptée aux applications de petite ou moyenne taille ou à faible croissance, car elle peut être coûteuse et complexe à mettre en œuvre et à maintenir. Il est important de bien évaluer les exigences en termes de scalabilité, de flexibilité, de coûts et de délai, afin de choisir l'architecture la plus adaptée à votre projet.


## En Résumé :

Chaque type d'architecture web présente ses propres avantages et inconvénients, qui doivent être pris en compte lors du choix de l'architecture. Voici quelques exemples :

- **Avantages de l'architecture monolithe** :
  - Simplicité de mise en œuvre et de déploiement
  - Faibles coûts de développement et de maintenance
  - Facilité de modification et de mise à jour de l'application

- **Inconvénients de l'architecture monolithe** :
  - Difficulté à scaler et à évoluer l'application à mesure qu'elle grandit
  - Faible flexibilité et réutilisabilité des composants de l'application
  - Risque de dépendance forte entre les composants de l'application

- **Avantages de l'architecture microservices** :
  - Grande flexibilité et réutilisabilité des microservices
  - Meilleure scalabilité et disponibilité de l'application
  - Facilité de modification et de mise à jour des microservices indépendamment les uns des autres

- **Inconvénients de l'architecture microservices** :
  - Complexité de mise en œuvre et de déploiement du fait de la nécessité de gérer un grand nombre de microservices
  - Coûts de développement et de maintenance plus élevés
  - Risque de dépendance forte entre les microservices

- **Avantages de l'architecture Serverless** :
  - Très grande scalabilité et disponibilité de l'application
  - Faibles coûts à mesure que l'application grandit
  - Faible latence et temps de réponse des fonctions

- **Inconvénients de l'architecture Serverless** :
  - Complexité de mise en œuvre et de déploiement
  - Coûts de développement et de maintenance plus élevés
  - Risque de dépendance forte entre les fonctions

Il est important de prendre en compte ces avantages et inconvénients lors du choix de l'architecture web, en fonction des besoins et des objectifs de l'application.

# Acteurs et protocoles de communication en architecture web

Dans une architecture web, il y a plusieurs acteurs qui jouent un rôle clé dans la communication et l'interaction entre les différents éléments de l'application. Ces acteurs sont le client, le serveur et le réseau.

```
          +--------------------+
          |      Client        |
          +--------------------+
                  |
             Requête HTTP 
                  |               
                  V               
          +--------------------+
          |      Réseau        |
          +--------------------+
                 |
             Requête HTTP 
                  |               
                  V         
          +--------------------+
          |      Serveur       |
          +--------------------+

```

## Le client

Le client est l'application ou le dispositif qui envoie une demande de données ou de services à un serveur. En architecture web, le client peut être un navigateur web (comme Chrome, Firefox ou Safari), une application mobile (comme une application Android ou iOS), ou tout autre dispositif qui peut envoyer des requêtes HTTP (Hypertext Transfer Protocol) à un serveur.

## Le serveur

Le serveur est l'application ou le dispositif qui reçoit les demandes de données ou de services envoyées par le client, et qui envoie une réponse en retour. En architecture web, le serveur peut être un serveur web (comme Apache ou Nginx), un serveur d'application (comme Tomcat ou Wildfly), ou tout autre dispositif qui peut recevoir des requêtes HTTP et envoyer des réponses.

### Serveur Web :

Un serveur web est un logiciel qui exécute sur un ordinateur et qui est conçu pour accepter des requêtes HTTP (Hypertext Transfer Protocol) en provenance de clients, tels que des navigateurs web, et pour renvoyer des réponses HTTP à ces clients. Les serveurs web sont souvent utilisés pour héberger des sites web, c'est-à-dire pour stocker, traiter et fournir les fichiers qui composent les pages web aux utilisateurs sur Internet.

Les serveurs web sont généralement exécutés sur des ordinateurs qui sont connectés à Internet en permanence et qui sont configurés pour accepter des connexions réseau entrantes. Lorsqu'un client envoie une requête HTTP à un serveur web, le serveur analyse la requête et envoie une réponse appropriée au client, qui peut être une page web, une image, un fichier audio ou tout autre type de données.

Il existe plusieurs types de serveurs web, y compris les serveurs web Apache, Nginx et Microsoft IIS, qui sont tous largement utilisés sur Internet. En général, les serveurs web sont configurés et gérés par des administrateurs système ou des développeurs web, qui s'assurent que le serveur fonctionne correctement et sécurisément.

### Serveur d'application :

Un serveur d'application est un logiciel qui exécute sur un ordinateur et qui est conçu pour gérer les applications et les services qui sont accessibles sur un réseau. Les serveurs d'application sont généralement utilisés pour fournir une interface de programmation (API) qui peut être utilisée par d'autres applications ou par des utilisateurs pour accéder à ces services.

Les serveurs d'application sont souvent utilisés pour exécuter des applications de gestion de bases de données, des applications de gestion de contenu, des applications de commerce électronique et de nombreuses autres applications qui nécessitent une interface de programmation pour être accessibles par d'autres logiciels ou par des utilisateurs finaux. Ils peuvent également être utilisés pour fournir des services tels que l'authentification, l'autorisation et la gestion des utilisateurs à d'autres applications.

Il existe plusieurs types de serveurs d'application, tels que les serveurs d'application Java, les serveurs d'application Microsoft .NET et les serveurs d'application Ruby on Rails, Python Django ... En général, les serveurs d'application sont configurés et gérés par des administrateurs système, SRE, Devops ou des développeurs d'application, qui s'assurent que le serveur fonctionne correctement et sécurisément.

### Serveur de base de données :

Un serveur de base de données est un logiciel qui exécute sur un ordinateur et qui est conçu pour stocker et gérer les données dans une base de données. Les bases de données sont utilisées pour stocker et organiser de grandes quantités de données de manière structurée, de sorte qu'elles puissent être facilement consultées, mises à jour et gérées.

Les serveurs de base de données sont souvent utilisés pour stocker et gérer les données de grandes organisations, telles que les entreprises, les gouvernements et les universités. Ils offrent une interface de programmation (API) qui peut être utilisée par d'autres applications ou par des utilisateurs pour accéder et gérer les données dans la base de données.

Il existe plusieurs types de serveurs de base de données, tels que MySQL, Microsoft SQL Server et Oracle, qui sont tous largement utilisés dans de nombreux domaines. En général, les serveurs de base de données sont configurés et gérés par des administrateurs de base de données, qui s'assurent que le serveur fonctionne correctement et sécurisément.

## Le réseau

Le réseau est l'ensemble des équipements et des protocoles qui permettent la communication entre le client et le serveur. En architecture web, le réseau peut être le réseau local (LAN), le réseau étendu (WAN), ou Internet.

## Protocoles de communication


Un protocole de communication est un ensemble de règles et de conventions qui définissent comment deux ou plusieurs parties (par exemple, des ordinateurs, des serveurs, des appareils mobiles) peuvent échanger des informations sur un réseau (par exemple, Internet, un LAN). Il permet de standardiser la manière de formater, de transmettre et de recevoir les données, afin de garantir une compréhension mutuelle et une interaction fiable entre les parties.



## QCM : Introduction à l'architecture web


Voici un exemple de 5 questions qui peuvent tomber lors d'un examen :

```
1. Qu'est-ce que l'architecture web ?
a) Un ensemble de technologies et de protocoles qui permettent de transférer des données sur un réseau, principalement sur Internet
b) Un système de gestion de contenu qui permet de publier et de gérer des sites web
c) Un système d'exploitation qui permet d'exécuter des applications web
d) Aucune de ces réponses n'est correcte

2. Qu'est-ce qu'un serveur de base de données ?
a) Un ordinateur ou un logiciel qui permet de stocker, de gérer et de fournir des données (par exemple, des informations sur les clients ou les produits) sur un réseau, principalement sur Internet
b) Un navigateur web qui permet de consulter des données sur un réseau, principalement sur Internet
c) Un protocole de communication qui permet de transférer des données sur un réseau, principalement sur Internet
d) Aucune de ces réponses n'est correcte

3. Qu'est-ce qu'un serveur web ?
a) Un ordinateur ou un logiciel qui permet de stocker, de gérer et de fournir des ressources (pages web, images, fichiers, etc.) sur un réseau, principalement sur Internet
b) Un navigateur web qui permet de consulter des ressources sur un réseau, principalement sur Internet
c) Un protocole de communication qui permet de transférer des données sur un réseau, principalement sur Internet
d) Aucune de ces réponses n'est correcte

4. Qu'est-ce qu'un serveur d'application ?
a) Un ordinateur ou un logiciel qui permet de stocker, de gérer et de fournir des ressources (pages web, images, fichiers, etc.) sur un réseau, principalement sur Internet
b) Un navigateur web qui permet de consulter des ressources sur un réseau, principalement sur Internet
c) Un protocole de communication qui permet de transférer des données sur un réseau, principalement sur Internet
d) Un ordinateur ou un logiciel qui permet d'exécuter des applications (par exemple, une application de gestion de contacts ou de gestion de projets) sur un réseau, principalement sur Internet

5. Qu'est-ce qu'un client ?
a) Un ordinateur ou un logiciel qui permet de stocker, de gérer et de fournir des ressources (pages web, images, fichiers, etc.) sur un réseau, principalement sur Internet
b) Un navigateur web qui permet de consulter des ressources sur un réseau, principalement sur Internet
c) Un protocole de communication qui permet de transférer des données sur un réseau, principalement sur Internet
d) Un ordinateur ou un logiciel qui permet d'exécuter des applications (par exemple, une application de gestion de contacts ou de gestion de projets) sur un réseau, principalement sur Internet

```


## Exercice : modéliser une architecture web en utilisant un diagramme de cas d'utilisation

Vous pouvez utiliser un outil de diagramme de cas d'utilisation comme Lucidchart ou Draw.io pour réaliser votre modélisation. Voici quelques éléments à prendre en compte lors de la création de votre diagramme :

- Identifiez les cas d'utilisation de votre application web (par exemple : naviguer parmi les produits, ajouter un produit au panier, finaliser un achat, etc.)
- Définissez les acteurs de votre application web (par exemple : utilisateur, administrateur, système de paiement, etc.)
- Tracez les liens entre les cas d'utilisation et les acteurs en utilisant des flèches
- Ajoutez des notes pour expliquer les détails de chaque cas d'utilisation

Voici un exemple de diagramme de cas d'utilisation pour un site de e-commerce :

```
         +------------+
         | Utilisateur|
         +------------+
             |  |
          +--|--+
          |  |  |
          |  |  |
  +-------------------+
  |    Système de    |
  |   paiement       |
  +-------------------+
          |  |  |
          |  |  |
          +--|--+
             |  |
         +------------+
         | Administrateur|
         +------------+


```

Votre cas d'étude sera le réseau instagram, pour faciliter l'exercice on exclu volontairement la partie "chat" et "story" de l'application.