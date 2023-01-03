---
title: "Session 3 : Introduction à l'architecture web"
date: 2022-12-29T10:00:16+01:00
draft: false
---

# Les différents éléments d'une application web

Le front end et le backend sont deux parties d'une application web qui travaillent ensemble pour fournir une expérience utilisateur cohérente.

#### Front end
Le front end, également appelé "client", se réfère aux éléments d'une application web qui sont visibles et interagissables par l'utilisateur. Il comprend généralement du HTML, du CSS et du JavaScript qui sont exécutés dans le navigateur de l'utilisateur. Le front end se concentre sur l'apparence et l'expérience utilisateur de l'application, en gérant les éléments de l'interface utilisateur tels que les formulaires, les boutons et les menus.

#### Backend
Le backend, également appelé "serveur", se réfère aux éléments d'une application web qui sont exécutés côté serveur et qui sont généralement invisibles pour l'utilisateur. Il comprend généralement du code qui s'exécute sur un serveur web et qui est responsable de la gestion des données, de la logique métier et des communications avec les bases de données et d'autres services. Le backend peut être implémenté à l'aide de différents langages de programmation et de frameworks, tels que Java, .NET ou Node.js.

#### Bases de données
Les bases de données sont des systèmes de gestion de données qui permettent de stocker, de gérer et de récupérer des données de manière structurée et efficace. Elles sont souvent utilisées en conjonction avec des applications web pour stocker et gérer les données de l'application, telles que les utilisateurs, les produits et les transactions. Il existe plusieurs types de bases de données, comme les bases de données relationnelles (SQL) et les bases de données non relationnelles (NoSQL), qui sont adaptées à différents types de données et de scénarios d'utilisation.


# Les différentes technologies utilisées pour mettre en œuvre une architecture web (Java, .NET, Node.js, Python Django, etc.)

Il existe de nombreuses technologies qui peuvent être utilisées pour mettre en œuvre une architecture web. Chacune de ces technologies a ses propres caractéristiques et spécificités, qui en font un choix plus ou moins adapté selon les besoins et les contextes de l'application.

#### Java
Java est un langage de programmation populaire et polyvalent, qui est utilisé pour développer des applications web côté serveur. Il est souvent utilisé avec des frameworks tels que Spring ou Hibernate, qui facilitent la mise en œuvre de l'architecture backend de l'application. Java est particulièrement adapté aux applications à grande échelle et aux environnements distribués, grâce à sa robustesse, sa portabilité et sa sécurité.

#### .NET
.NET est un framework de développement Microsoft qui fournit un ensemble d'outils et de bibliothèques pour développer des applications web côté serveur (backend). Il est principalement utilisé avec le langage de programmation C#, mais il supporte également d'autres langages tels que F# ou VB.NET. .NET est particulièrement adapté aux applications d'entreprise et aux environnements Microsoft, grâce à sa puissance, sa flexibilité et sa compatibilité avec les autres technologies Microsoft.

#### Node.js
Node.js est un environnement d'exécution JavaScript côté serveur (backend), qui permet de développer des applications web en utilisant le même langage côté serveur (backend) et côté client. Il est basé sur le moteur JavaScript V8 de Google Chrome et utilise un modèle d'exécution asynchrone pour gérer les requêtes HTTP et les événements de manière performante. Node.js est particulièrement adapté aux applications en temps réel et aux environnements de microservices, grâce à sa légèreté, sa rapidité et sa scalabilité.

#### Python Django
Django est un framework de développement web open source basé sur le langage de programmation Python. Il fournit un ensemble de bibliothèques et d'outils pour développer rapidement et facilement des applications web côté serveur (backend). Django est particulièrement adapté aux applications web de petite et moyenne envergure, grâce à sa simplicité, sa flexibilité et sa puissance. Il est souvent utilisé pour développer des applications web à fort contenu dynamique, comme des blogs, des sites de commerce électronique ou des réseaux sociaux.


# La création d’un environnement de développement et de déploiement pour les services web (outils de build, de test, de déploiement, etc.)

## Le cycle de vie d'une application :

Lorsqu'on développe et déploie des services web, il est important de mettre en place un environnement de développement et de déploiement adapté et optimisé. Cet environnement doit permettre de gérer les différentes étapes du cycle de vie de l'application, depuis la création du code jusqu'à la mise en production, en passant par le test et la validation.

## Les différents environements :

Il existe plusieurs types d'environnements informatiques, qui peuvent être utilisés à différentes fins et dans différentes situations. Voici quelques exemples courants :

1. _Environnement de développement_ (dev): Cet environnement est utilisé par les développeurs pour créer, tester et déboguer du code. Il peut inclure des outils de développement, des bibliothèques et des frameworks, ainsi que des émulateurs ou des simulateurs pour tester le code sur différentes plateformes ou dans différentes conditions.

2. _Environnement de staging_ (staging): Cet environnement est utilisé pour préparer et tester le code et les applications avant qu'ils ne soient déployés en production. Il peut être configuré de manière similaire à l'environnement de production, afin de permettre aux équipes de vérifier comment le code et les applications se comporteront une fois en production.

3. _Environnement de production_ (prod): Cet environnement est utilisé pour exécuter le code et les applications de manière permanente et pour les rendre disponibles aux utilisateurs finaux. Il peut inclure des serveurs de production, des bases de données et d'autres équipements de production, ainsi que des outils de gestion et de surveillance pour surveiller et gérer l'environnement de production.


Il est important de maintenir des environnements séparés pour chaque étape du développement et du déploiement, afin de s'assurer que le code et les applications sont testés et débogués correctement avant d'être mis en production. Cela peut aider à éviter les erreurs et les problèmes de performance en production. Il est également à noter que le nombre d'environement varie selon les entreprises.


## Git Workflow :

Un workflow Git est un ensemble de règles et de pratiques qui définissent la manière dont une équipe de développement utilise et gère un système de contrôle de version (SCV) tel que Git. Un workflow Git peut inclure des règles sur la manière de créer et de fusionner des branches, de rédiger des messages de commit, de gérer les conflits, de publier du code, etc.

Il existe plusieurs workflow Git possibles, qui peuvent être adaptés aux besoins et aux contextes de l'équipe de développement. Voici quelques exemples de workflow Git couramment utilisés :

-  Le workflow Github Flow est un workflow Git qui a été conçu par l'équipe de développement de Github. Il se base sur la création de branches pour chaque fonctionnal

- _Workflow centralisé_ : Le workflow centralisé est le plus simple et le plus classique des workflow Git. Il se base sur un dépôt centralisé (sur un serveur ou sur un service en ligne) qui sert de référence commune pour tous les membres de l'équipe. Chaque membre peut créer des branches à partir de ce dépôt central et y apporter des modifications, qui doivent être validées et fusionnées par un responsable avant d'être publiées.

- _Workflow Git Flow_ : Le workflow Git Flow est un workflow Git qui se base sur la création de branches spécifiques pour les fonctionnalités, les corrections de bugs et les versions de production. Ce workflow est particulièrement adapté aux projets de grande envergure et aux équipes organisées en mode agile.

- _Workflow Kanban Flow_ : Le workflow Kanban Flow est un workflow Git qui s'inspire du modèle Kanban de gestion de projet. Il se base sur la création de tâches et de cartes dans un tableau Kanban, qui représentent les différentes étapes du développement (à faire, en cours, terminé, etc.). Chaque carte peut être associée à une branche Git, qui contient le code correspondant à cette tâche. Le workflow Kanban Flow permet de visualiser et de suivre l'avancement du projet en temps réel, et de s'adapter aux changements de priorité et de contexte.


Comme ce n'est pas l'object principal de ce cours voici une [vidéo](https://www.youtube.com/watch?v=1SXpE08hvGs) qui devrait vous aider à mieux comprendre. Il est très important (si ce n'est *vital*) de comprendre cette notion si vous travaillez en entreprise.

Bien que souvent lié nous allons ici faire 2 partie distintes pour la CI/CD.

## Intégration continue (CI) :

L'intégration continue (CI) est une pratique de développement de logiciel qui consiste à intégrer les modifications et les ajouts de code de manière régulière et automatisée dans le code source principal du projet. L'objectif de l'intégration continue est de s'assurer que le code source est stable et fonctionnel à tout moment, en détectant et en corrigeant les erreurs et les bugs de manière précoce.

Pour mettre en place une intégration continue, il est nécessaire de configurer un environnement de développement et de déploiement automatisé, qui inclut des outils de build, de test et de déploiement. Ces outils permettent de construire, de tester et de déployer le code source de manière automatisée, en s'appuyant sur un système de contrôle de version (Git, SVN, etc.) et sur un serveur d'intégration continue (Jenkins, Travis CI, etc.).

L'intégration continue s'appuie sur une stratégie de développement en continu, qui consiste à développer et à intégrer le code de manière continue et itérative, plutôt que de le faire de manière séquentielle et ponctuelle. Cette stratégie permet de réduire les temps de développement et de déploiement, de s'assurer de la qualité et de la stabilité du code, et de faciliter la collaboration et la communication au sein de l'équipe de développement.

#### Outils de build
Les outils de build sont des logiciels qui permettent de *compiler*, d'assembler et de packager le code source de l'application en vue de sa mise en production. Ils peuvent automatiser et optimiser différentes tâches de build, comme la génération de fichiers binaires, la création de fichiers de configuration, l'inclusion de dépendances, la minification de code, etc. Exemples d'outils de build : Maven, Gradle, Ant, Webpack.

Remarque :

Il existe deux grandes catégories de langages de programmation : les langages compilés et les langages interprétés.

##### Langages compilés

Les langages compilés sont des langages qui nécessitent d'être compilés avant d'être exécutés. La compilation consiste à traduire le code source du langage en un code exécutable, qui sera ensuite envoyé à la machine pour être exécuté. Les langages compilés sont généralement plus efficaces et plus rapides à l'exécution, mais nécessitent un temps de compilation plus long et ne sont pas aussi flexibles que les langages interprétés. Exemples de langages compilés : C, C++, C#, Golang.
##### Langages interprétés

Les langages interprétés sont des langages qui sont exécutés directement, sans passer par une étape de compilation. L'interpréteur lit et exécute le code source ligne par ligne, en traduisant au fur et à mesure le code en instructions exécutables par la machine. Les langages interprétés sont généralement plus simples à utiliser et à déboguer, mais sont moins efficaces et plus lents à l'exécution que les langages compilés. Exemples de langages interprétés : Python, PHP, Ruby, JavaScript.

##### Difference entre les deux types de language :

*Temps de compilation* : Les langages compilés nécessitent un temps de compilation plus long pour traduire le code source en code exécutable, alors que les langages interprétés sont exécutés directement sans passer par cette étape.

*Efficacité et performance* : En général, les langages compilés sont plus efficaces et plus rapides à l'exécution que les langages interprétés, car le code exécutable produit par la compilation est optimisé pour la machine et bénéficie de toutes les optimisations du compilateur. Les langages interprétés sont généralement plus lents à l'exécution, car l'interpréteur doit traduire et exécuter le code source ligne par ligne.

*Flexibilité et simplicité* : Les langages interprétés sont généralement plus flexibles et plus simples à utiliser que les langages compilés, car ils permettent de tester et de déboguer le code de manière plus rapide et interactive. Les langages compilés nécessitent souvent de recompiler le code avant de pouvoir le tester, ce qui peut être plus long et fastidieux.

*Maintenance et évolutivité* : Les langages compilés nécessitent souvent plus de maintenance et sont moins évolutifs que les langages interprétés, car ils nécessitent de recompiler le code avant de le tester ou de le déployer. Les langages interprétés permettent généralement de mettre à jour le code de manière plus rapide et interactive, sans avoir à recompiler tout le programme.

*Sécurité* : Les langages compilés sont généralement considérés comme plus sûrs que les langages interprétés, car le code exécutable produit par la compilation est difficilement lisible et modifiable par un tiers. Les langages interprétés, en revanche, permettent généralement de lire et de modifier facilement le code source, ce qui peut poser des problèmes de sécurité si le code contient des failles ou des vulnérabilités.

*Environnement de développement* : Les langages compilés nécessitent souvent un environnement de développement spécifique, avec des outils de compilation et de déploiement, alors que les langages interprétés peuvent souvent être utilisés avec un simple éditeur de texte et un interpréteur en ligne de commande.

#### Outils de test :

Les outils de test sont des logiciels qui permettent de vérifier et de valider le bon fonctionnement et la qualité de l'application. Ils peuvent exécuter différents types de tests, comme les tests unitaires, les tests d'intégration, les tests de performance, les tests de sécurité, etc. Les résultats des tests sont généralement reportés dans des rapports, qui permettent de suivre l'état de l'application et de détecter les éventuels problèmes. Exemples d'outils de test : JUnit, TestNG, Selenium, JMeter.

Il existe différent types de test : 

##### Tests de performance :

Les tests de performance sont des tests qui mesurent les indicateurs de performance d'un système, tels que sa vitesse, sa capacité de traitement, sa fiabilité, etc. Ils permettent de s'assurer que le système est capable de gérer les charges de travail prévues et de répondre aux exigences de performance définies. Les tests de performance sont souvent exécutés par les testeurs ou les administrateurs système au cours de la phase de déploiement, pour valider les performances du système en conditions réelles.


##### Tests de sécurité :

Les tests de sécurité sont des tests qui vérifient la sécurité d'un système, en détectant et en corrigeant les failles et les vulnérabilités qui pourraient être exploitées par des attaquants. Ils permettent de s'assurer que le système est protégé contre les menaces externes et internes, et qu'il respecte les règles de sécurité en vigueur. Les tests de sécurité sont souvent exécutés par des experts en sécurité ou des sociétés de testing spécialisées, pour valider la sécurité du système avant son déploiement.

##### Tests d'acceptation :

Les tests d'acceptation sont des tests qui vérifient que le système répond aux besoins et aux attentes des utilisateurs ou des clients. Ils permettent de s'assurer que le système est facile à utiliser, ergonomique et fonctionnel, et qu'il respecte les standards et les normes en vigueur. Les tests d'acceptation sont souvent exécutés par les utilisateurs ou les clients finaux au cours de la phase de déploiement, pour valider l'adéquation du système aux besoins et aux attentes de l'organisation.


## Déploiement continue (CD) :

Le déploiement continu (Continuous Deployment en anglais) est une pratique de développement logiciel qui consiste à automatiser et à intégrer de manière continue les étapes de build, de test et de déploiement d'une application. Le but du déploiement continu est de permettre une livraison rapide et fréquente de nouvelles fonctionnalités et de corrections de bugs, tout en maintenant un niveau élevé de qualité et de stabilité du code.

Pour mettre en œuvre le déploiement continu, il est nécessaire de mettre en place une chaîne d'intégration et de déploiement (CI/CD en anglais) qui permet de gérer de manière automatisée et transparente les différentes étapes du processus de déploiement. La CI/CD peut être basée sur des outils de build, de test et de déploiement tels que Jenkins, Travis CI, CircleCI, etc.

Voici quelques exemples de scénarios de déploiement continu :

- Déploiement continu sur un serveur de staging : Dans ce scénario, chaque fois qu'un développeur valide un commit sur la branche de développement, le processus de CI/CD déclenche automatiquement la compilation et les tests de l'application, puis déploie le code sur un serveur de staging (environnement de préproduction). Les tests de non-régression et les validations manuelles peuvent être effectuées sur ce serveur avant de déclencher le déploiement sur le serveur de production.

- Déploiement continu sur le serveur de production : Dans ce scénario, le processus de CI/CD déploie automatiquement le code sur le serveur de production dès qu'il est validé sur la branche de développement. Cette approche est plus risquée, car elle nécessite de mettre en place des tests de qualité et de stabilité très rigoureux pour éviter les erreurs de déploiement.

- Déploiement continu sur le cloud : Dans ce scénario, le processus de CI/CD déploie automatiquement l'application sur un environnement de cloud computing, comme AWS ou Google Cloud. Cette approche permet de bénéficier d'une scalabilité et d'une flexibilité importantes, ainsi que d'une facilité de gestion et de maintenance.


### Outils de déploiement :

Les outils de déploiement sont des logiciels qui permettent de déployer l'application sur un ou plusieurs serveurs de production. Ils peuvent automatiser et optimiser différentes tâches de déploiement, comme le transfert de fichiers, la configuration de l'application, le redémarrage de services, la mise à jour de la base de données, etc. Ils peuvent également gérer les différentes versions de l'application et les rollbacks en cas de problème. Exemples d'outils de déploiement : Jenkins, Github Action, Gitlab CI, ArgoCD ...


## La gestion des erreurs et des exceptions dans les services web :

La gestion des erreurs et des exceptions est un élément clé de la conception et de la maintenance des services web. Elle permet de détecter et de traiter les problèmes qui peuvent survenir lors de l'exécution de l'application, afin d'assurer sa stabilité et sa qualité.

Voici quelques exemples concrets de gestion des erreurs et des exceptions dans les services web :

- Les erreurs de syntaxe : il s'agit d'erreurs qui surviennent lors de la compilation du code, lorsque celui-ci n'est pas conforme aux règles du langage de programmation utilisé. Par exemple, si vous oubliez un ";" à la fin d'une instruction en Java, vous obtiendrez une erreur de syntaxe lors de la compilation. Ces erreurs sont généralement détectées et corrigées au moment de la compilation.

    
- Les erreurs de runtime : il s'agit d'erreurs qui surviennent lors de l'exécution du code, lorsque celui-ci tente d'accéder à des ressources ou de manipuler des données de manière incorrecte. Par exemple, si vous essayez de lire un fichier qui n'existe pas, vous obtiendrez une erreur de runtime. Ces erreurs peuvent être gérées en utilisant des blocs de gestion d'exceptions (try-catch en Java, try-except en Python, etc.). Par exemple, en Java, vous pouvez utiliser le code suivant pour gérer une erreur de runtime :

```python
try {
  // Code qui peut générer une erreur de runtime
} catch (Exception e) {
  // Traitement de l'erreur
}
```

- Les erreurs de communication : il s'agit d'erreurs qui surviennent lors de l'échange de données entre les différents composants de l'application, en cas de problèmes de réseau, de protocole ou de format. Par exemple, si vous envoyez une requête HTTP à un serveur qui ne répond pas, vous obtiendrez une erreur de communication. Ces erreurs peuvent être gérées en utilisant des codes de statut HTTP et en traitant les réponses en conséquence. Par exemple, en utilisant l'API Fetch de JavaScript, vous pouvez utiliser le code suivant pour gérer une erreur de communication :

```JavaScript
fetch('https://example.com/api/endpoint')
  .then(response => {
    if (response.ok) {
      // Traitement de la réponse
    } else {
      // Traitement de l'erreur de communication
    }
  })
  .catch(error => {
    // Traitement de l'erreur de communication
  });

```

# Exercice : Mise en place d'un workflow GitOps pour le déploiement d'une application web

En groupe de 4 étudiants, vous allez devoir imaginer et mettre en place un workflow GitOps pour le déploiement d'une application web (celle de votre choix). Vous devrez prendre en compte les éléments suivants dans votre workflow :

- La gestion des sources de code : comment gérer les versions et les branches de votre application ? Qui est responsable de la review du code et comment se fait-elle ?
- La gestion des builds et des tests : comment automatiser la compilation et les tests de votre application ? Qui est responsable de la vérification de la qualité du code et comment se fait-elle ?
- La gestion des déploiements : comment déployer votre application sur différents environnements (développement, staging, production) ? Qui est responsable de la validation des déploiements et comment se fait-elle ?
- La gestion des rollbacks : comment gérer les cas où un déploiement ne se passe pas comme prévu et il faut revenir à une version précédente de l'application ?
- La documentation : comment documenter votre workflow de manière à ce qu'il soit facilement compréhensible et reproductible par d'autres membres de l'équipe ?

Pour réaliser cet exercice, vous devrez imaginer un workflow GitOps adapté aux besoins de votre application et le mettre en place sur un repository Git. Vous devrez également documenter votre workflow de manière à ce qu'il soit facilement compréhensible par d'autres membres de l'équipe.

Note : vous pouvez utiliser des outils tels que GitLab, Jenkins ou GitHub Actions pour mettre en place votre workflow.