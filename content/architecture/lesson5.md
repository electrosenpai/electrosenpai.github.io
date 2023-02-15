---
title: "Session 5 : Monitoring et logging des services web"
date: 2022-12-29T10:00:16+01:00
draft: false
---

# Introduction :

Le monitoring et le logging sont des pratiques clés pour assurer la disponibilité, la performance et la sécurité des services web.

## Monitoring :

Le monitoring est la surveillance continue d'un système ou d'une application pour détecter les anomalies et les problèmes potentiels. Il permet de mesurer les performances et les métriques d'un système, telles que la charge de traitement, la mémoire utilisée, les entrées/sorties disque, etc. Ces données peuvent être utilisées pour détecter les problèmes potentiels, comme des ralentissements inattendus, des erreurs, ou des épuisements de ressources, et pour les corriger avant qu'ils ne causent des perturbations ou des interruption de service.



## Logging :

Le logging est l'enregistrement de données sur l'état et les activités d'un système. Il permet de récupérer des informations sur les erreurs et les anomalies qui se produisent, et de les utiliser pour résoudre les problèmes, comprendre les tendances et identifier les tendances à venir. Les données de journalisation peuvent également être utilisées pour répondre aux exigences réglementaires ou pour la conformité.

En utilisant des technologies de monitoring comme Datadog, les administrateurs de systèmes peuvent surveiller les performances de leurs services web en temps réel, collecter des métriques et des données de journalisation de leurs applications, et utiliser des alertes et des rapports pour identifier les problèmes potentiels avant qu'ils ne causent des perturbations de service.

En résumé, le monitoring et le logging sont des pratiques clés pour assurer la disponibilité, la performance et la sécurité des services web. Les données collectées par le monitoring et le logging peuvent être utilisées pour détecter les problèmes potentiels, comprendre les tendances et identifier les tendances à venir, et pour répondre aux exigences réglementaires ou pour la conformité. Les technologies de monitoring comme Datadog permettent aux administrateurs de systèmes de surveiller les performances de leurs services web en temps réel, collecter des métriques et des données de journalisation de leurs applications, et utiliser des alertes et des rapports pour identifier les problèmes potentiels avant qu'ils ne causent des perturbations de service.


Ainsi, avec le monitoring, on peut suivre l'état des différents composants de l'architecture des services web, par exemple, les serveurs web, les bases de données, les services d'authentification, pour s'assurer qu'ils sont disponibles et performants. Cela nous permet de détecter les problèmes potentiels avant qu'ils n'affectent les utilisateurs. Le monitoring peut également aider à comprendre les tendances de charge et de trafic, et à planifier les ressources nécessaires pour gérer les pics de trafic.

Le logging permet quant à lui de stocker des informations sur les interactions avec les services web, cela peut inclure les erreurs, les requêtes, les réponses et les actions de l'utilisateur. Ces informations peuvent être utilisées pour résoudre les problèmes, comprendre les tendances et identifier les tendances à venir. Les données de journalisation peuvent également être utilisées pour répondre aux exigences réglementaires ou pour la conformité.

Enfin, utiliser des outils de monitoring et de logging tels que Datadog permet de centraliser les données de différents composants de l'architecture de services web, de les visualiser et de les analyser facilement. Les alertes peuvent être configurées pour alerter les administrateurs de système en cas de problème, ce qui permet de réagir rapidement et de résoudre les problèmes avant qu'ils ne causent des perturbations de service. Les données collectées peuvent également être utilisées pour créer des tableaux de bord et des rapports pour suivre les performances et les tendances au fil du temps.

En utilisant des outils de monitoring et de logging, les administrateurs de systèmes peuvent surveiller les performances des services web en temps réel, détecter les problèmes potentiels avant qu'ils ne causent des perturbations de service, et répondre aux exigences réglementaires et à la conformité.

Cela dit, il est important de noter que la sécurité de ces outils de monitoring et de logging doit être prise en considération pour éviter les fuites de données ou les accès non autorisés aux données collectées. Il est donc essentiel de mettre en place les protocoles de sécurité adéquats et de suivre régulièrement les politiques de sécurité.

# Logging et monitoring en python :

Python dispose d'une bibliothèque de journalisation intégrée appelée logging, qui permet de générer des messages de journalisation de manière simple et efficace. Il est également possible d'utiliser des bibliothèques de monitoring telles que psutil pour récupérer des informations sur les performances et les ressources système.

Voici quelques exemples d'utilisation de la journalisation et du monitoring en Python :

## Journalisation de base :

```python
import logging

logging.basicConfig(level=logging.INFO,
                    format='%(asctime)s %(levelname)s %(message)s')

logging.info("Application started")
logging.warning("A warning message")
logging.error("An error occurred")

```

## Monitoring de la mémoire utilisée :

```python
import psutil

memory_info = psutil.virtual_memory()
print("Total memory: ", memory_info.total)
print("Used memory: ", memory_info.used)
print("Available memory: ", memory_info.available)
```

## Monitoring de l'utilisation du processeur :

```python
import psutil

cpu_info = psutil.cpu_percent(interval=1)
print("CPU usage: ", cpu_info)
```

## Journalisation et monitoring combinés :

```python
import logging
import psutil

logging.basicConfig(level=logging.INFO,
                    format='%(asctime)s %(levelname)s %(message)s')

logging.info("Application started")

# Perform calculations
result = 0
for i in range(1, 101):
    result += i
    cpu_info = psutil.cpu_percent()
    logging.info("CPU usage: %s", cpu_info)

logging.info("Application finished")
```

Il est important de noter que les exemples ci-dessus ne représentent qu'une petite partie des fonctionnalités offertes par les bibliothèques de journalisation et de monitoring disponibles en Python. Il est donc important de consulter la documentation de ces bibliothèques pour en savoir plus sur les fonctionnalités

# Les outils pour du monitoring et log

Dans cette partie nous allons regarder les outils les plus utilisés pour le monitoring.

## Datadog :

Datadog est un outil de monitoring et d'analyse des performances pour les applications et les infrastructures. Il permet de collecter, stocker et afficher les données de performance en temps réel provenant de différentes sources, comme des applications, des serveurs, des réseaux, etc. Il fournit également des fonctionnalités d'analyse pour identifier les tendances et les problèmes éventuels dans les données de performance.

Il y a plusieurs façons d'intégrer Datadog à vos applications et à votre infrastructure. Il est possible de collecter des données de performance à l'aide d'agents légers installés sur les serveurs, ou en utilisant des API pour envoyer des données à partir des applications. Il est également possible de connecter Datadog à des services externes tels que AWS, Azure, GCP, etc.

Une fois les données collectées, Datadog les stocke dans un système de stockage distribué et les affiche à l'aide de tableaux de bord interactifs. Il permet également de créer des alertes pour des valeurs limites spécifiques, pour une utilisation de ressources anormale, des erreurs, etc.

Il offre également des fonctionnalités avancées telles que l'analyse des journaux, la surveillance de l'infrastructure, la surveillance de l'application, l'analyse de la performance des requêtes, etc.

Datadog est particulièrement utile pour les équipes de développement, les équipes de DevOps et les équipes de gestion de la performance pour identifier les problèmes de performances et les résoudre rapidement. Il est également très utile pour les équipes de sécurité pour identifier les problèmes de sécurité potentiels.

Il est important de noter que pour utiliser les fonctionnalités avancées de Datadog il est nécessaire de souscrire à un abonnement payant, mais il propose également une version gratuite avec des fonctionnalités limitées.

Si vous le souhaitez et à la place de l'exercice donné dans ce cours vous pouvez faire à la place le cours 101 de Datadog. Ce [cours](https://learn.datadoghq.com/courses/dd-101-dev)peut vous amener à une certification. (ce qui peut grandement vous aidez pour votre recherche d'alternance et/ou de travail plus tard)

## Grafana & Prometheus :

Grafana est un outil open-source de visualisation de données et de monitoring. Il permet de créer des tableaux de bord interactifs pour afficher les données de performance en temps réel à partir de différentes sources de données. Il prend en charge de nombreux formats de données courants, notamment InfluxDB, Graphite, Elasticsearch, Prometheus, etc.

Il est possible de connecter Grafana à des bases de données pour récupérer des données de performance, et utiliser ces données pour créer des graphiques et des tableaux de bord personnalisés. Il offre également des fonctionnalités avancées telles que l'analyse de tendances, l'alerte en temps réel, la collaboration en temps réel, etc.

Grafana est particulièrement utile pour les équipes de développement, les équipes de DevOps et les équipes de gestion de la performance pour identifier les problèmes de performances et les résoudre rapidement. Il est également très utile pour les équipes de sécurité pour identifier les problèmes de sécurité potentiels.

Prometheus est un système de surveillance open-source qui permet de collecter des données de performance en temps réel à partir de différentes sources. Il utilise un langage de requête pour interroger les données de performance et fournit des fonctionnalités de visualisation de base. Il prend en charge de nombreux formats de données courants, notamment les données de performance de système, les métriques d'application, les journaux, etc.

Prometheus est particulièrement utile pour les équipes de développement, les équipes de DevOps et les équipes de gestion de la performance pour identifier les problèmes de performances et les résoudre rapidement. Il est également très utile pour les équipes de sécurité pour identifier les problèmes de sécurité potentiels. Il est souvent utilisé conjointement avec Grafana pour une meilleure visualisation des données.

Il est important de noter que Prometheus est un projet open-source qui est souvent utilisé en conjonction avec d'autres outils tels que Grafana pour une meilleure visualisation des données. Si vous souhaitez essayer Grafana vous pouvez faire un tour sur ce [site](https://play.grafana.org/)

# QCM :

Qu'est-ce que le monitoring ?
a. La surveillance continue d'un système ou d'une application pour détecter les anomalies et les problèmes potentiels.
b. La collecte de données de performance pour identifier les tendances.
c. La visualisation de données en temps réel.
d. La mise en place de protocoles de sécurité.
Réponse : a

Qu'est-ce que le logging ?
a. La collecte de données de performance pour identifier les tendances.
b. L'enregistrement de données sur l'état et les activités d'un système.
c. La surveillance continue d'un système ou d'une application pour détecter les anomalies et les problèmes potentiels.
d. La mise en place de protocoles de sécurité.
Réponse : b

Comment peut-on détecter les problèmes potentiels avec le monitoring ?
a. En mesurant les performances et les métriques d'un système.
b. En visualisant les données en temps réel.
c. En collectant des données de performance pour identifier les tendances.
d. En stockant des informations sur les interactions avec les services web.
Réponse : a

Comment peut-on utiliser les données de journalisation ?
a. Pour identifier les problèmes potentiels.
b. Pour comprendre les tendances et identifier les tendances à venir.
c. Pour répondre aux exigences réglementaires ou pour la conformité.
d. Toutes les réponses sont correctes.
Réponse : d

Comment peut-on centraliser les données de différents composants de l'architecture de services web ?
a. En utilisant des technologies de monitoring comme Datadog.
b. En utilisant des protocoles de sécurité adéquats.
c. En surveillant les performances des services web en temps réel.
d. En stockant des informations sur les interactions avec les services web.
Réponse : a

Que peut-on surveiller avec le monitoring ?
a. Les serveurs web.
b. Les bases de données.
c. Les services d'authentification.
d. Toutes les réponses sont correctes.
Réponse : d

Que peut-on stocker avec le logging ?
a. Les interactions avec les services web.
b. Les performances et les métriques d'un système.
c. Les données de performance pour identifier les tendances.
d. Les protocoles de sécurité adéquats.
Réponse : a

Comment peut-on réagir rapidement en cas de problème ?
a. En configurant des alertes pour alerter les administrateurs de système.
b. En stockant des informations sur les interactions avec les services web.
c. En utilisant des bibliothèques de monitoring telles que psutil.
d. En créant des tableaux de bord et des rapports.
Réponse : a

Comment peut-on détecter les problèmes de performances et les résoudre rapidement ?
a. En utilisant Datadog.
b. En utilisant Grafana.
c. En utilisant Prometheus.
d. Toutes les réponses sont correctes.
Réponse : d

Quels types de données peut-on collecter avec Datadog ?
a. Des données de performance provenant de différentes sources.
b. Des données de performance provenant d'applications uniquement.
c. Des données de performance provenant de serveurs uniquement.
d. Des données de performance provenant de réseaux uniquement.
Réponse : a

Quel est l'outil open-source de visualisation de données et de monitoring qui permet de créer des tableaux de bord interactifs pour afficher les données de performance en temps réel à partir de différentes sources de données ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : b) Grafana

Quel est le système de surveillance open-source qui permet de collecter des données de performance en temps réel à partir de différentes sources et qui utilise un langage de requête pour interroger les données de performance ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : c) Prometheus

Quel outil de monitoring permet de collecter, stocker et afficher les données de performance en temps réel provenant de différentes sources, comme des applications, des serveurs, des réseaux, etc. ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : a) Datadog

Quel outil de monitoring permet de connecter Grafana à des bases de données pour récupérer des données de performance, et utiliser ces données pour créer des graphiques et des tableaux de bord personnalisés ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : b) Grafana

Quel outil de monitoring permet de collecter des données de performance à l'aide d'agents légers installés sur les serveurs, ou en utilisant des API pour envoyer des données à partir des applications, et de connecter à des services externes tels que AWS, Azure, GCP, etc. ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : a) Datadog

Quel est l'outil de monitoring et d'analyse des performances pour les applications et les infrastructures qui offre des fonctionnalités avancées telles que l'analyse des journaux, la surveillance de l'infrastructure, la surveillance de l'application, l'analyse de la performance des requêtes, etc. ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : a) Datadog

Quel outil de monitoring permet de créer des alertes pour des valeurs limites spécifiques, pour une utilisation de ressources anormale, des erreurs, etc. ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : a) Datadog

Quel outil de monitoring est particulièrement utile pour les équipes de développement, les équipes de DevOps et les équipes de gestion de la performance pour identifier les problèmes de performances et les résoudre rapidement, ainsi que pour les équipes de sécurité pour identifier les problèmes de sécurité potentiels ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : a) Datadog

Quel outil de monitoring est souvent utilisé conjointement avec Grafana pour une meilleure visualisation des données ?
a) Datadog
b) Grafana
c) Prometheus
d) Azure Monitor

Réponse : c) Prometheus