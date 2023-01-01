---
title: "Session 2 : Conception d’une architecture web "
date: 2022-12-29T10:00:16+01:00
draft: false
---

## Les critères de choix d'une architecture web

Lorsqu'on doit décider quelle architecture adopter pour une application web, il est important de prendre en compte plusieurs critères qui vont influencer sa performance, sa scalabilité et sa flexibilité. Voici quelques exemples de critères à prendre en compte :

- Scalabilité : la capacité d'un système à s'adapter et à évoluer en fonction de la croissance de la demande en termes de ressources, de performance et de fonctionnalités.
- Flexibilité : la capacité d'un système à évoluer et à s'adapter rapidement aux changements de requirements ou de contexte.
- Fiabilité : la capacité d'un système à fonctionner de manière stable et sans interruption.
- Coût : le coût total de possession (TCO) d'un système, c'est-à-dire tous les coûts associés à son développement, son déploiement et son maintenance. On peut également parler de FinOps
- Sécurité : la capacité d'un système à protéger les données et les ressources contre les attaques ou les accès non autorisés.

Il est important de peser chaque critère et de déterminer lesquels sont les plus importants en fonction des besoins de l'application.

## La modélisation des services web avec les diagrammes de séquence et de cas d'utilisation

La modélisation des services web peut être faite à l'aide de différents diagrammes, notamment les diagrammes de séquence et de cas d'utilisation.

Le diagramme de séquence permet de modéliser les interactions entre les différents éléments d'un système, en particulier les échanges de messages entre les services. Il permet de visualiser l'ordre dans lequel les messages sont envoyés et reçus, ainsi que les conditions de déclenchement de chaque message.

Voici un exemple de diagramme de séquence modélisant l'interaction entre un client et un service web :


```
Client Service web
-----------------> Requête HTTP ----------------->
(GET /resource)
<----------------- Réponse HTTP <-----------------
(200 OK)
```


Le diagramme de cas d'utilisation permet de modéliser les différentes actions que peuvent réaliser les utilisateurs d'un système, ainsi que les rôles et les responsabilités de chaque acteur impliqué. Il permet de visualiser les limites et les contraintes du système, ainsi que les interactions avec d'autres systèmes ou services.

Voici un exemple de diagramme de cas d'utilisation modélisant l'interaction entre un client et un service web :


```
       +---------------+
       |  Client       |
       +---------------+
       |               |
       |   Afficher    |
       |   ressource   |
       |               |
       |  Requête HTTP |
       |  (GET /resource)
       |               |
       |  Réponse HTTP |
       |  (200 OK)     |
       |               |
       +---------------+
            |   |
            |   |
            v   v
       +---------------+
       |  Service web  |
       +---------------+
```


## Les patterns d'architecture web couramment utilisés

Il existe plusieurs patterns d'architecture web couramment utilisés pour modéliser et construire des applications distribuées. Voici quelques exemples de patterns fréquemment utilisés :

### API Gateway :

Une API Gateway est une passerelle de communication qui sert de point d'entrée unique et centralisé pour les différents services et composants de l'application. Elle permet de mettre en place une interface de communication standardisée et normalisée, en gérant les routes, les protocoles, les sécurités, les performances, etc. L'API Gateway s'appuie sur des technologies comme les APIs REST, les WebHooks, les Events, etc. pour gérer les échanges de données et de messages entre les différents acteurs de l'application.

## Pourquoi utiliser une API Gateway ?

Il y a plusieurs raisons pour lesquelles il peut être judicieux d'utiliser une API Gateway :

- Simplification et sécurisation de l'intégration et de l'interopérabilité des services : l'API Gateway permet de masquer et d'abstraire les implémentations et les spécificités des services, en leur proposant une interface commune et normalisée. Cela facilite et sécurise l'intégration et l'interopérabilité des services, en évitant les redondances et les erreurs de communication.

- Gestion des routes et des protocoles : l'API Gateway permet de gérer les routes et les protocoles de communication entre les différents services et composants de l'application. Elle peut par exemple rediriger les requêtes vers les services concernés, en fonction de leur URL ou de leur verbe HTTP. Elle peut également gérer les différents protocoles de communication, en les adaptant aux besoins et aux contextes de l'application.

- Gestion des sécurités et des performances : l'API Gateway permet de mettre en place des mécanismes de sécurité et de performance pour protéger et optimiser l'accès aux services. Elle peut par exemple gérer les authentifications, les autorisations, les quotas, les caches, les compressions, etc. pour assurer la sécurité et la performance de l'application.


### Exemple :

Voici quelques exemples d'utilisation d'une API Gateway :

- Gestion des demandes de trafic : Une API Gateway peut être utilisée pour gérer les demandes de trafic et répartir les requêtes entre les différents services qui composent l'application.
- Sécurité : Une API Gateway peut être utilisée pour mettre en place des contrôles de sécurité, tels que l'authentification et l'autorisation, avant que les requêtes ne soient transmises aux services cibles.
- Transformation des requêtes : Une API Gateway peut être utilisée pour transformer les requêtes entrantes afin de les adapter aux spécificités des services cibles. Par exemple, elle peut ajouter ou retirer des en-têtes, ou encore convertir les données de la requête dans un format différent.
- Monitoring et suivi des erreurs : Une API Gateway peut être utilisée pour surveiller les performances des services et détecter les erreurs, afin de permettre une meilleure gestion de la disponibilité de l'application.

Voici quelques exemples de logiciels d'API Gateway :

- Amazon API Gateway : Ce service de cloud computing proposé par Amazon Web Services permet de créer, publier, maintenir et surveiller des APIs pour connecter les applications avec les données et les fonctionnalités de l'application.
- Kong : Cette plateforme open source d'API Gateway permet de gérer les requêtes entrantes, de sécuriser les communications et de surveiller les performances des APIs.
- Tyk : Cette plateforme open source d'API Gateway offre une large gamme de fonctionnalités, y compris la gestion du trafic, la sécurisation des communications et la surveillance des performances.
- Express Gateway : Cette solution open source basée sur Node.js est conçue pour être facile à utiliser et à déployer, et offre des fonctionnalités de gestion du trafic, de sécurité et de surveillance des performances.

### Load Balancing :

Le load balancing est une technique utilisée pour répartir la charge de travail sur plusieurs serveurs ou instances de traitement afin d'optimiser la performance et la disponibilité d'un système. Il est souvent utilisé dans les environnements de production pour gérer les pics de charge et assurer la continuité de service.

Il existe plusieurs types de load balancing, notamment le load balancing de niveau 7 (basé sur les couches 7 du modèle OSI) et le load balancing de niveau 4 (basé sur les couches 4 du modèle OSI). Le load balancing de niveau 7 prend en compte les informations de l'application, comme les en-têtes HTTP, pour déterminer comment répartir la charge de travail. Le load balancing de niveau 4 se base uniquement sur les informations de transport, comme l'adresse IP et le numéro de port, pour répartir la charge de travail.

Le load balancing peut être mis en place de différentes manières, comme en utilisant un équilibreur de charge dédié ou en utilisant un logiciel de load balancing sur un serveur existant. Il est également possible de configurer le load balancing en utilisant un service de cloud computing, comme Amazon Elastic Load Balancing ou Google Cloud Load Balancer.

#### Load balancer :

Un load balancer (équilibreur de charge) est un composant ou un service qui permet de répartir la charge de travail sur plusieurs serveurs ou instances de traitement afin d'optimiser la performance et la disponibilité d'un système. Il est généralement utilisé dans les environnements de production pour gérer les pics de charge et assurer la continuité de service.

Il existe plusieurs technologies et logiciels qui peuvent être utilisés pour mettre en place un load balancer, parmi lesquels :

* HAProxy : un logiciel open source qui permet de mettre en place un load balancer de niveau 7 (basé sur les couches 7 du modèle OSI) sur n'importe quel système d'exploitation.
* NGINX : un serveur web open source qui peut être utilisé comme load balancer de niveau 7 ou de niveau 4 (basé sur les couches 4 du modèle OSI).
* Amazon Elastic Load Balancer (ELB) : un service de cloud computing proposé par Amazon Web Services qui permet de mettre en place un load balancer de niveau 4 ou de niveau 7 sur l'infrastructure cloud d'AWS (attention le niveau 7 s'appelle un ALB).
* Google Cloud Load Balancer : un service de cloud computing proposé par Google Cloud Platform qui permet de mettre en place un load balancer de niveau 4 ou de niveau 7 sur l'infrastructure cloud de Google.


### Circuit Breaker :

- Circuit Breaker : ce pattern consiste à mettre en place un mécanisme de protection pour prévenir les erreurs de cascades et les dégradations de performance dans un environnement distribué. Le Circuit Breaker permet de couper temporairement l'accès à un service défaillant, afin de limiter les dommages et de permettre une récupération progressive.

Un circuit breaker est un patron de conception qui permet de protéger une application contre les pannes de sous-systèmes en désactivant temporairement les appels de service à ces sous-systèmes qui échouent de manière répétée.

Le circuit breaker suit un processus simple :
- 1. Lorsqu'un appel de service échoue, le circuit breaker enregistre cet échec.
- 2. Si un nombre suffisamment élevé d'appels de service échouent de manière consécutive, le circuit breaker passe en mode "ouvert" et bloque tous les appels de service futurs vers le sous-système en question.
- 3. Pendant que le circuit breaker est ouvert, il surveille en continu si les appels de service réussissent à nouveau.
- 4. Si un nombre suffisamment élevé d'appels de service réussissent de manière consécutive, le circuit breaker passe en mode "fermé" et autorise à nouveau les appels de service vers le sous-système.

L'utilisation d'un circuit breaker offre plusieurs avantages, tels que :
- La protection contre les pannes de sous-systèmes : en désactivant temporairement les appels de service qui échouent de manière répétée, l'application est protégée contre les pannes de sous-systèmes qui pourraient la mettre hors service.
- La réduction de la charge sur le sous-système : en bloquant les appels de service vers le sous-système en panne, la charge sur celui-ci est réduite, ce qui peut lui permettre de se rétablir plus rapidement.
- La gestion des temps de réponse : en désactivant temporairement les appels de service qui prennent trop de temps, l'application peut mieux gérer ses temps de réponse et éviter les retards.

#### Exemple :

Voici quelques exemples d'utilisation de circuit breaker :

- Dans une application de commerce en ligne, un circuit breaker peut être utilisé pour protéger l'application contre les pannes du système de paiement. Si le système de paiement échoue de manière répétée, le circuit breaker peut être activé pour bloquer temporairement les appels de service vers ce système et empêcher l'application de se bloquer.

- Dans une application de gestion de ressources humaines, un circuit breaker peut être utilisé pour protéger l'application contre les pannes du système de gestion des salaires. Si le système de gestion des salaires échoue de manière répétée, le circuit breaker peut être activé pour bloquer temporairement les appels de service vers ce système et empêcher l'application de se bloquer.

- Dans une application de gestion de projets, un circuit breaker peut être utilisé pour protéger l'application contre les pannes du système de gestion des tâches. Si le système de gestion des tâches échoue de manière répétée, le circuit breaker peut être activé pour bloquer temporairement les appels de service vers ce système et empêcher l'application de se bloquer.

Voici quelques exemples de logiciels qui sont conçus pour fonctionner en tant que circuit breaker :

- Hystrix : Cette bibliothèque open source, développée par Netflix, est spécialement conçue pour implémenter des circuit breakers dans les applications Java.
- Resilience4j : Cette bibliothèque open source est également conçue pour implémenter des circuit breakers dans les applications Java, mais elle est plus légère et plus facile à utiliser que Hystrix.
- Fuse : Ce logiciel commercial est conçu pour implémenter des circuit breakers dans les applications .NET.
- Envoy : Cette bibliothèque open source, développée par Lyft, est conçue pour implémenter des circuit breakers et d'autres fonctionnalités de gestion de la disponibilité dans les applications distribuées.


### Cache :

- Cache : ce pattern consiste à mettre en place un mécanisme de mémorisation de données fréquemment utilisées, afin de réduire les temps de réponse et de soulager la charge sur les services backend. Le Cache peut être configuré pour stocker des données en mémoire, sur disque ou dans un système de stockage distribué, en fonction de différents critères de validité et de fréquence d'utilisation.

Le cache est une mémoire tampon qui stocke temporairement des données afin de réduire le temps de réponse lorsqu'elles sont demandées à nouveau. Il s'agit d'un mécanisme de mémoire intermédiaire qui permet d'accélérer l'accès aux données en les mettant à disposition sans avoir à les requérir à chaque fois auprès de leur source d'origine.

Voici quelques exemples d'utilisation de cache :

- Dans un navigateur web : Le cache du navigateur web stocke temporairement les pages web et leurs éléments (images, scripts, etc.) afin de réduire le temps de chargement lorsqu'elles sont visitées à nouveau.
- Dans un serveur web : Le cache du serveur web peut être utilisé pour stocker les réponses aux requêtes HTTP afin de réduire la charge sur le serveur et d'accélérer le temps de réponse pour les utilisateurs.
- Dans un système de fichiers : Le cache du système de fichiers peut être utilisé pour stocker les données de fichiers récemment lus afin de réduire le temps d'accès aux données lorsqu'elles sont demandées à nouveau.
- Dans une base de données : Le cache de base de données peut être utilisé pour stocker temporairement les données de base de données fréquemment utilisées afin de réduire le temps de réponse des requêtes de base de données.

Voici quelques exemples de logiciels de cache :

- Memcached : C'est un système de cache en mémoire distribué open source utilisé pour stocker temporairement des données de base de données, de fichiers ou d'autres informations structurées. Il est souvent utilisé pour accélérer les applications web en réduisant la charge sur les bases de données et les serveurs de fichiers.
- Redis : C'est un système de cache en mémoire open source qui permet de stocker temporairement des données de différents types (chaînes de caractères, listes, ensembles, etc.) et qui prend en charge diverses opérations de traitement de données. Il est souvent utilisé comme base de données de cache, comme système de message ou comme outil de traitement de données en temps réel.
- Varnish : C'est un logiciel de cache de serveur web open source qui permet de stocker temporairement les réponses aux requêtes HTTP afin de réduire la charge sur le serveur web et d'accélérer le temps de réponse pour les utilisateurs. Il peut être configuré pour cacher des pages web, des images et d'autres éléments de contenu en fonction de différents critères.
- Squid : C'est un serveur proxy open source qui permet de stocker temporairement les réponses aux requêtes HTTP et HTTPS afin de réduire la charge sur les serveurs web et d'accélérer le temps de réponse pour les utilisateurs. Il peut être configuré pour cacher des pages web, des images et d'autres éléments de contenu en fonction de différents critères.

### Event Bus :

- Event Bus : ce pattern consiste à mettre en place un mécanisme de communication asynchrone entre les différents éléments d'une application, en utilisant un bus de messages ou un système de notification. L'Event Bus permet de découpler les échanges de messages entre les services, de manière à améliorer la flexibilité et la robustesse de l'application.

Il s'agit d'une couche de communication indépendante qui permet de decoupler les différents services et composants de l'application, de manière à ce qu'ils n'aient pas à se connaître ou à se dépendre les uns des autres. 

Un Event Bus peut être mis en place sous différentes formes, comme par exemple :
- Un bus de messages : qui permet de publier et de souscrire à des messages asynchrones, en utilisant un broker de messages comme RabbitMQ, Kafka, etc.
- Un bus d'événements : qui permet de publier et de souscrire à des événements asynchrones, en utilisant un système de gestion d'événements comme AWS EventBridge, Azure Event Grid, etc.
- Un bus de notifications : qui permet de publier et de souscrire à des notifications asynchrones, en utilisant un système de notifications comme AWS SNS, Azure Notification Hubs, etc.

L'utilisation d'un Event Bus permet de bénéficier de plusieurs avantages, comme par exemple :
- La decoupling : qui permet de séparer les différents services et composants de l'application, de manière à ce qu'ils n'aient pas à se connaître ou à se dépendre les uns des autres.
- La scalabilité : qui permet de gérer de manière plus efficace les volumes de trafic et de charge, en répartissant la charge sur plusieurs instances et en ne bloquant pas les services en cas de problème.
- La flexibilité : qui permet de s'adapter rapidement aux changements et aux évolutions de l'application, en modifiant ou en ajoutant facilement de nouveaux services ou de nouvelles fonctionnalités.

## Exercice : concevoir une architecture web en utilisant les différents outils vus en cours

Vous pouvez utiliser un outil de diagramme de cas d'utilisation comme Lucidchart ou Draw.io pour réaliser votre modélisation. Voici quelques éléments à prendre en compte lors de la création de votre diagramme :

- Prenez le cas d'une application de e-commerce qui permet de acheter en ligne des produits.
- Identifiez les différents services nécessaires à l'application (par exemple : service de gestion des produits, service de gestion des commandes, service de gestion des utilisateurs, etc.)
- Utilisez des diagrammes de séquence et de cas d'utilisation pour modéliser les interactions entre ces services.
- Choisissez un pattern d'architecture web qui convient à votre application (par exemple, API Gateway, Load Balancer, Circuit Breaker, etc.) et justifiez votre choix.
- Dessinez le diagramme de votre architecture en utilisant les outils vus en cours (par exemple, draw.io).
- Rédigez un rapport décrivant votre architecture et les résultats de vos tests.