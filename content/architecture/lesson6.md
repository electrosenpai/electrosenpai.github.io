---
title: "Session 6 : Évolution et maintenance des services web"
date: 2022-12-29T10:00:16+01:00
draft: false
---

# Concepts de base

## Architecture des services web
Les services web sont construits sur une architecture client-serveur, similaire à celle utilisée pour les sites web. Le client (qui peut être un navigateur web, une application mobile, ou un autre service web) envoie une requête à un serveur web, qui traite la requête et renvoie une réponse au client. Les services web peuvent utiliser différents protocoles de communication, tels que HTTP (HyperText Transfer Protocol), SOAP (Simple Object Access Protocol), ou REST (Representational State Transfer).

## Protocoles et normes associés aux services web
Les protocoles et normes associés aux services web permettent de décrire les services, les messages échangés, les interfaces, et les opérations supportées. Par exemple :

- WSDL (Web Services Description Language) est un langage de description de service qui permet de décrire les opérations du service, les types de données échangés, et les protocoles de communication utilisés.
- XML (Extensible Markup Language) est un langage de balisage qui permet de décrire les données échangées entre le client et le serveur. XML est souvent utilisé pour encapsuler les données dans les messages échangés entre le client et le serveur.
- JSON (JavaScript Object Notation) est un format de données léger et facile à lire qui est souvent utilisé pour les services web RESTful. JSON est souvent utilisé pour encapsuler les données dans les messages échangés entre le client et le serveur.

## Notions de service, d'interface, de message et de transport
Un service web est une fonction ou un ensemble de fonctions exposées via une interface standardisée. L'interface décrit les opérations du service, les messages échangés, et les formats de message. Par exemple, un service web qui fournit des informations sur la météo peut avoir une interface qui définit une opération "getWeather" qui prend en entrée une ville et une date, et renvoie les prévisions météorologiques pour cette ville à cette date.

Les messages sont les données échangées entre le client et le serveur. Les messages peuvent contenir des données structurées (par exemple, une liste d'objets météo pour différentes heures de la journée) ou des données binaires (par exemple, une image ou un fichier audio). Les messages sont souvent encapsulés dans des formats de données tels que XML ou JSON.

Le transport définit la manière dont les messages sont envoyés. Le protocole HTTP est souvent utilisé pour le transport des messages dans les services web. Les messages peuvent être envoyés via une requête HTTP POST ou GET, avec des données encapsulées dans le corps de la requête. Les services web SOAP utilisent un protocole similaire, mais avec une syntaxe de message différente.

## Modèles de développement de services web

Il existe plusieurs modèles de développement de services web, chacun avec ses propres caractéristiques, avantages et inconvénients. Les trois modèles les plus couramment utilisés sont :

- Le modèle RPC (Remote Procedure Call) : Ce modèle est basé sur les appels de procédures distantes, où le client appelle une fonction exposée par le serveur et attend une réponse. Le serveur traite la demande et renvoie une réponse à l'appelant. Ce modèle est similaire à l'appel de méthode locale, mais la fonction est exécutée sur le serveur distant. Le modèle RPC est souvent utilisé avec le protocole SOAP.

- Le modèle documentaire : Ce modèle est basé sur la manipulation de documents, tels que XML ou JSON, plutôt que sur des appels de procédures distantes. Le client envoie un document au serveur qui le traite et renvoie un document en réponse. Ce modèle est souvent utilisé avec le protocole RESTful.

- Le modèle RESTful : Ce modèle est basé sur les principes de l'architecture REST (Representational State Transfer). Le client envoie des requêtes HTTP au serveur pour effectuer des opérations sur des ressources (par exemple, un document XML ou une base de données). Le serveur renvoie une réponse HTTP, généralement au format JSON. Le modèle RESTful est de plus en plus populaire en raison de sa simplicité et de sa flexibilité.

Dans les prochaines parties de ce cours, nous allons explorer en détail l'évolution et la maintenance des services web, ainsi que les bonnes pratiques pour les développer de manière évolutives et maintenables.


# Évolution des services web

## Besoins d'évolution
Les besoins d'évolution des services web sont nombreux et peuvent inclure des changements de besoins des utilisateurs, des changements de la législation ou des normes, des changements de technologie, ou des corrections de bugs. Les besoins d'évolution peuvent être mineurs, comme la correction d'un bug mineur, ou majeurs, comme l'ajout de nouvelles fonctionnalités importantes.

## Approches d'évolution
Il existe plusieurs approches pour l'évolution des services web, selon les besoins spécifiques. Les approches les plus courantes sont :

- L'évolution compatible : Cette approche consiste à ajouter de nouvelles fonctionnalités sans affecter les anciennes. Par exemple, si un service web fournit une opération "getWeather", il peut être étendu pour fournir une nouvelle opération "getHistoricalWeather" sans affecter l'opération existante. Cette approche est souvent utilisée lorsque les clients existants ne doivent pas être modifiés.

- L'évolution incompatible : Cette approche consiste à modifier l'interface du service de manière à ce que les clients existants ne puissent plus l'utiliser sans modification. Par exemple, si un service web expose une opération "getWeather" qui renvoie un objet de type "Weather", il peut être modifié pour renvoyer un objet de type "WeatherForecast" avec des données supplémentaires. Cette approche est souvent utilisée lorsque les changements sont majeurs et que les clients existants doivent être mis à jour.

- Le versioning : Cette approche consiste à maintenir plusieurs versions du service web simultanément, afin de permettre aux clients de choisir la version qui convient le mieux à leurs besoins. Par exemple, si un service web a une nouvelle version qui ajoute de nouvelles fonctionnalités, les clients peuvent continuer à utiliser l'ancienne version si elle répond mieux à leurs besoins. Cette approche est souvent utilisée lorsque les changements sont majeurs et que les clients existants ne peuvent pas être mis à jour facilement.

## Stratégies de migration
La migration d'un service web d'une version à une autre peut être complexe et nécessite une planification soigneuse. Les stratégies de migration les plus courantes sont :

- La migration en douceur : Cette stratégie consiste à mettre à jour le service web et les clients en même temps, de manière à minimiser les perturbations pour les utilisateurs. Cette stratégie est souvent utilisée lorsque les changements sont mineurs.

- La migration par étapes : Cette stratégie consiste à mettre à jour le service web et les clients par étapes successives, en s'assurant que chaque étape est testée et validée avant de passer à la suivante. Cette stratégie est souvent utilisée lorsque les changements sont majeurs et que les risques de perturbation sont élevés.

## Pratiques de gestion de la compatibilité ascendante et descendante
La gestion de la compatibilité ascendante et descendante est essentielle pour assurer une évolution réussie des services web. La compatibilité ascendante garantit que les nouvelles versions du service



# Les différentes approches pour évoluer et maintenir une architecture web :

Il y a plusieurs approches pour évoluer et maintenir une architecture web, notamment le versioning, la compatibilité ascendante et la planification des mises à jour.

## Versioning :

Il s'agit de donner des numéros de version à votre application ou à ses composants, de manière à pouvoir identifier facilement les différentes versions d'une application. Cela permet de gérer les différentes versions de l'application de manière efficace et de garantir la compatibilité entre les différentes versions. Il existe différents formats de versionnement tels que la norme semantic versioning (SemVer) qui est un format standard pour versioning les logiciels.

## Rétro Compatibilité  :

Il s'agit de garantir que les nouvelles versions d'une application sont compatibles avec les anciennes versions. Cela permet aux utilisateurs de mettre à jour l'application sans avoir à se soucier de la compatibilité avec d'autres composants de leur système. Cela peut être accompli en utilisant des techniques telles que l'utilisation de bibliothèques de compatibilité, en garantissant la compatibilité des API, en maintenant une documentation complète et en effectuant des tests de compatibilité réguliers.

1. Planification des mises à jour : Il est important de planifier les mises à jour de l'application de manière à minimiser les perturbations pour les utilisateurs. Cela peut être accompli en effectuant des mises à jour en dehors des heures de pointe, en communiquant clairement les modifications apportées à l'application et en fournissant une formation pour les utilisateurs sur les nouvelles fonctionnalités.

2. Gestion des dépendances : Une bonne gestion des dépendances est cruciale pour évoluer et maintenir une architecture web. Il est important de maintenir à jour les dépendances de l'application et de s'assurer qu'elles sont compatibles avec les dernières versions. Il est également important de tenir un inventaire des dépendances utilisées dans l'application et de s'assurer qu'elles sont régulièrement mises à jour.

3. Documenter les modifications : Il est important de documenter les modifications apportées à l'application, afin de faciliter la maintenance et le dépannage futurs. Cela peut inclure la documentation des modifications apportées aux fonctionnalités de l'application, des modifications apportées à la base de données et des modifications apportées aux dépendances de l'application.

En utilisant ces approches, vous pouvez évoluer et maintenir efficacement une architecture web en garantissant la compatibilité, la planification des mises à jour et la gestion des dépendances.

## Équipe de développement dédiée :

 Il est important d'avoir une équipe dédiée pour gérer les tâches liées à l'évolution et à la maintenance de l'architecture web. Cela peut inclure la gestion des mises à jour, la résolution de bogues, la surveillance des performances et la planification des nouvelles fonctionnalités. Cela permet de garantir que l'application reste stable et fonctionnelle à tout moment.

## Tests automatisés :

Les tests automatisés sont un outil précieux pour garantir la qualité de l'application lors des mises à jour et des modifications. Il est important de mettre en place des tests unitaires, des tests d'intégration et des tests de performance pour s'assurer que l'application fonctionne correctement après les mises à jour.


## Monitoring en continu :

Il est important de surveiller en continu les performances de l'application pour détecter les problèmes potentiels avant qu'ils ne causent des perturbations pour les utilisateurs. Il est possible d'utiliser des outils de monitoring tels que Prometheus, Datadog ou Grafana pour surveiller les performances de l'application en temps réel et recevoir des alertes en cas de problème.

## Utilisation de conteneurs :

Les conteneurs sont de plus en plus utilisés pour empaqueter et déployer des applications. Ils permettent de créer des environnements de développement et de production identiques, ce qui facilite la maintenance de l'application. Les conteneurs peuvent être utilisés pour encapsuler les dépendances de l'application et pour faciliter les mises à jour et les rollbacks en cas de problème.

## Microservices architecture: 

L'utilisation de l'architecture Microservices permet de découper une application en plusieurs services indépendants qui communiquent entre eux via des API. Cela facilite la maintenance et l'évolution de l'application car les services peuvent être mis à jour ou remplacés indépendamment les uns des autres. Cela permet également de gérer les différentes parties de l'application de manière plus efficace en utilisant des technologies et des outils spécifiques pour chaque service.

# La gestion des dépendances et des bibliothèques utilisées par les services web:

La gestion des dépendances et des bibliothèques utilisées par les services web est essentielle pour garantir la qualité, la sécurité et la fiabilité de votre application. Il existe plusieurs approches pour gérer les dépendances de votre application, notamment la gestion manuelle, l'utilisation de gestionnaires de paquets et l'utilisation de conteneurs.

1. Gestion manuelle : Cette approche consiste à gérer manuellement les dépendances de l'application en téléchargeant et en installant les bibliothèques nécessaires sur chaque serveur ou poste de développement. Cette approche peut être fastidieuse et sujette aux erreurs, surtout si l'application utilise de nombreuses dépendances.

2. Utilisation de gestionnaires de paquets : Les gestionnaires de paquets tels que pip pour Python, npm pour JavaScript ou Composer pour PHP, permettent de gérer les dépendances de l'application de manière automatisée. Il est possible de définir les dépendances de l'application dans un fichier de configuration, puis de les installer en utilisant un simple commande. Cette approche est plus efficace que la gestion manuelle, mais il est important de s'assurer que les dépendances sont à jour et sécurisées.

3. Utilisation de conteneurs : Les conteneurs permettent de gérer les dépendances de l'application en encapsulant l'application et ses dépendances dans un environnement isolé. Les dépendances sont définies dans un fichier de configuration de conteneur (Dockerfile par exemple) et sont automatiquement installées lorsque le conteneur est démarré. Cette approche est plus efficace que les approches précédentes car elle garantit que l'application fonctionne de manière identique sur tous les environnements. 

Il est important de noter que la gestion des dépendances inclut également la mise à jour régulière des dépendances pour garantir la sécurité et la fiabilité de l'application. Il est également important de tenir un inventaire des dépendances utilisées dans l'application pour s'assurer qu'elles sont régulièrement mises à jour. Il est également important de s'assurer que les dépendances utilisées sont licenciées de manière appropriée et ne posent pas de risques de sécurité.

En utilisant ces approches, vous pouvez gérer efficacement les dépendances de votre application en utilisant des outils automatisés et en garantissant la sécurité et la fiabilité de votre application. Il est important de mettre en place des processus et des outils pour gérer les dépendances de manière efficace afin de garantir la qualité de l'application et la sécurité des utilisateurs.

Il existe plusieurs logiciels qui peuvent aider à gérer la version de ces bibliothéques :

1. Dependency Management Tools : Ces outils sont spécifiques à un certain type de développement (Java, Python, NodeJS etc..) et permettent de gérer les dépendances de manière automatisée. Exemples: Maven pour Java, pip pour Python, npm pour NodeJS, Composer pour PHP, etc.

2. Outils de gestion de conteneurs : Les outils de gestion de conteneurs tels que Docker et Kubernetes permettent de gérer les dépendances en encapsulant l'application et ses dépendances dans un environnement isolé. Les dépendances sont définies dans un fichier de configuration de conteneur (Dockerfile par exemple) et sont automatiquement installées lorsque le conteneur est démarré.

3. Outils de gestion de paquet : Ces outils permettent de gérer les dépendances de manière automatisée. Exemples : apt pour Ubuntu, yum pour Red Hat, pacman pour Arch Linux, etc.

4. Outils de gestion de cycle de vie de dépendance : Ces outils permettent de gérer les dépendances en suivant leur cycle de vie. Exememples : JFrog Artifactory, Sonatype Nexus, Apache Archiva, etc.

Outils de gestion de vulnérabilités : Ces outils permettent de scanner les dépendances pour détecter les vulnérabilités de sécurité. Exemples : Snyk, Dependabot, OWASP Dependency Check, etc.

En utilisant ces outils, vous pouvez gérer efficacement les dépendances de votre application en automatisant les tâches de gestion des dépendances, en garantissant la qualité de l'application, et en protégeant les utilisateurs contre les vulnérabilités de sécurité. Il est important de choisir les outils les plus adaptés à vos besoins pour gérer efficacement les dépendances de votre application.

## Les différentes techniques de déploiements :

Un déploiement blue-green est une technique de déploiement de l'application qui consiste à avoir deux ensembles de ressources (généralement deux instances de l'application) en cours d'exécution en parallèle, appelées "blue" (bleu) et "green" (vert). Les utilisateurs sont dirigés vers l'une des instances en cours d'exécution, généralement l'instance "blue" pendant que l'autre instance "green" est utilisée pour les mises à jour ou les tests.

Lorsque les mises à jour ou les tests sont terminés sur l'instance "green", les utilisateurs sont dirigés vers cette instance, devenant ainsi "live" et l'instance "blue" est utilisée pour les prochaines mises à jour ou les tests.

Cette technique permet de minimiser les perturbations pour les utilisateurs lors des mises à jour, car ils continuent à utiliser l'instance "live" pendant que les mises à jour sont effectuées sur l'instance "green", et de faciliter les rollbacks en cas de problème car il suffit de rediriger les utilisateurs vers l'instance précédemment utilisée.

Le déploiement blue-green est souvent utilisé en conjonction avec des outils de gestion de conteneurs pour automatiser les tâches de déploiement et de gestion des instances. Il est également utilisé pour les déploiements sur des plateformes cloud, qui offrent des fonctionnalités pour automatiser les tâches de déploiement, de scalabilité et de gestion des instances.

# Maintenance des services web

## Besoins de maintenance
La maintenance des services web est un processus continu qui vise à assurer le bon fonctionnement du service, la correction des bugs, la mise à jour des composants, et l'optimisation des performances. Les besoins de maintenance peuvent inclure la correction de bugs, l'ajout de fonctionnalités mineures, la mise à jour des bibliothèques logicielles, ou l'optimisation des performances.

## Pratiques de gestion de la qualité de service
La qualité de service (QoS) est essentielle pour assurer le bon fonctionnement des services web. Les pratiques de gestion de la QoS incluent :

- La surveillance des performances : Les performances du service web doivent être surveillées en continu pour détecter les problèmes et les goulots d'étranglement. Les indicateurs de performance tels que le temps de réponse, le taux d'erreur, et la disponibilité doivent être surveillés.

- La gestion de la capacité : La capacité du service web doit être gérée en fonction de la charge attendue. Les ressources du serveur doivent être allouées de manière optimale pour éviter les temps d'arrêt et les perturbations.

- La gestion des incidents : Les incidents tels que les erreurs de serveur, les pannes de réseau, et les problèmes de sécurité doivent être gérés de manière efficace pour minimiser les perturbations pour les utilisateurs.

## Pratiques de gestion de la configuration et du versioning
La gestion de la configuration et du versioning est essentielle pour assurer la maintenance réussie des services web. Les pratiques courantes incluent :

- La gestion des versions : Les versions du service web doivent être gérées de manière efficace pour permettre la mise à jour des clients existants et la gestion des versions antérieures du service.

- La gestion de la configuration : Les configurations du service web doivent être gérées de manière efficace pour permettre des mises à jour rapides et des rétablissements en cas de panne.

- La gestion du versioning de la base de données : Les mises à jour de la base de données sont courantes pour les services web. Il est donc important de gérer efficacement les versions de la base de données pour assurer la compatibilité ascendante et descendante.

## Pratiques de tests et de validation
Les pratiques de tests et de validation sont essentielles pour assurer la qualité et la fiabilité des services web. Les pratiques courantes incluent :

- Les tests unitaires : Les tests unitaires vérifient le bon fonctionnement des composants individuels du service web.

- Les tests d'intégration : Les tests d'intégration vérifient le bon fonctionnement du service web dans son ensemble.

- Les tests de charge : Les tests de charge vérifient les performances du service web sous charge.


# Exercice : Gestion de la qualité de service


Imaginez que vous travaillez pour une entreprise qui propose un service web de streaming vidéo. Le service est utilisé par des milliers d'utilisateurs à travers le monde, qui regardent des émissions de télévision et des films en streaming. L'entreprise souhaite améliorer la qualité de service de son service web pour réduire les temps de réponse et les interruptions de service.

- Expliquez pourquoi la qualité de service est importante dans ce scénario.

- Proposez une approche de gestion de la qualité de service pour améliorer les performances du service web sans perturber les utilisateurs existants.

- Décrivez les étapes de test et de validation que vous effectueriez pour vous assurer que les améliorations de performance ne perturbent pas les utilisateurs existants.

- Décrivez une procédure de préparation de mise à jour de composants applicatifs, quelles étapes feriez vous ?

# QCM :

Qu'est-ce que WSDL ?
a. Un format de données léger et facile à lire
b. Un langage de description de service
c. Un protocole de communication utilisé par les services web
d. Une interface standardisée pour les services web
Réponse : b

Quel est le protocole de communication le plus souvent utilisé dans les services web ?
a. HTTP
b. SOAP
c. REST
d. SMTP
Réponse : a

Qu'est-ce que la compatibilité ascendante ?
a. La garantie que les nouvelles versions d'une application sont compatibles avec les anciennes versions
b. La gestion des mises à jour de l'application
c. La rétrocompatibilité avec les anciennes versions d'une application
d. La planification des mises à jour pour minimiser les perturbations pour les utilisateurs
Réponse : c

Qu'est-ce que le modèle RPC ?
a. Un modèle basé sur la manipulation de documents tels que XML ou JSON
b. Un modèle basé sur les principes de l'architecture REST
c. Un modèle basé sur les appels de procédures distantes
d. Aucune des réponses ci-dessus
Réponse : c

Qu'est-ce que le format de versionnement SemVer ?
a. Un format de données léger et facile à lire
b. Un langage de description de service
c. Un protocole de communication utilisé par les services web
d. Un format standard pour versionner les logiciels
Réponse : d

Quel est le modèle le plus couramment utilisé pour les services web RESTful ?
a. Le modèle RPC
b. Le modèle documentaire
c. Le modèle RESTful
d. Aucune des réponses ci-dessus
Réponse : c

Qu'est-ce que la migration en douceur ?
a. Mettre à jour le service web et les clients en même temps, de manière à minimiser les perturbations pour les utilisateurs
b. Mettre à jour le service web et les clients par étapes successives
c. Garantir que les nouvelles versions d'une application sont compatibles avec les anciennes versions
d. Planifier les mises à jour de l'application de manière à minimiser les perturbations pour les utilisateurs
Réponse : a

Qu'est-ce que la gestion des dépendances ?
a. La gestion des changements de la législation ou des normes
b. La gestion des mises à jour de l'application
c. La gestion des bibliothèques utilisées par les services web
d. Aucune des réponses ci-dessus
Réponse : c

Qu'est-ce que JSON ?
a. Un langage de description de service
b. Un format de données léger et facile à lire
c. Un protocole de communication utilisé par les services web
d. Une interface standardisée pour les services web
Réponse : b

Qu'est-ce que la migration par étapes ?
a. Mettre à jour le service web et les clients en même temps, de manière à minimiser les perturbations pour les utilisateurs
b. Mettre à jour le service web et les clients par étapes successives
c. Garantir que les nouvelles versions d'une application sont compatibles avec les anciennes versions
d. Planifier les mises à jour de l'application



Quel est le langage de balisage utilisé pour décrire les données échangées entre le client et le serveur dans les services web ?
a) HTML
b) XML
c) JSON
d) CSS
Réponse : b) XML

Quel est le format de données léger et facile à lire souvent utilisé pour les services web RESTful ?
a) HTML
b) XML
c) JSON
d) CSS
Réponse : c) JSON

Qu'est-ce qu'un service web ?
a) Une interface standardisée exposée pour effectuer des opérations
b) Un langage de balisage utilisé pour décrire les données échangées
c) Le protocole utilisé pour le transport des messages dans les services web
d) Une fonctionnalité d'un site web
Réponse : a) Une interface standardisée exposée pour effectuer des opérations

Qu'est-ce qu'un message dans les services web ?
a) Une liste de protocoles de communication
b) Une image ou un fichier audio
c) Les données échangées entre le client et le serveur
d) Le format de données utilisé pour encapsuler les données dans les messages échangés
Réponse : c) Les données échangées entre le client et le serveur

Qu'est-ce que le transport dans les services web ?
a) La manière dont les messages sont envoyés
b) La description des opérations du service
c) Les données échangées entre le client et le serveur
d) Le format de données utilisé pour encapsuler les données dans les messages échangés
Réponse : a) La manière dont les messages sont envoyés

Quel est le modèle de développement de services web basé sur les principes de l'architecture REST ?
a) Le modèle RPC
b) Le modèle documentaire
c) Le modèle RESTful
d) Le modèle SOAP
Réponse : c) Le modèle RESTful

Quelle est l'approche d'évolution des services web qui consiste à ajouter de nouvelles fonctionnalités sans affecter les anciennes ?
a) L'évolution compatible
b) L'évolution incompatible
c) Le versioning
d) La migration en douceur
Réponse : a) L'évolution compatible

Quelle est l'approche de migration qui consiste à mettre à jour le service web et les clients en même temps, de manière à minimiser les perturbations pour les utilisateurs ?
a) La migration en douceur
b) La migration par étapes
c) L'évolution compatible
d) L'évolution incompatible
Réponse : a) La migration en douceur

Quelle est l'approche de gestion des dépendances qui permet de gérer les dépendances de l'application en encapsulant l'application et ses dépendances dans un environnement isolé ?
a) La gestion manuelle
b) L'utilisation de gestionnaires de paquets
c) L'utilisation de conteneurs
d) La migration en douceur
Réponse : c) L'utilisation de conteneurs

Quel est l'outil utilisé pour surveiller les performances de l'application en temps réel et recevoir des alertes en cas de problème ?
a) Prometheus
b) Datadog
c) Grafana
d) Tous les précédents
Réponse : d) Tous les précédents