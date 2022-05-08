---
lang: fr
---
# Devoxx 2022

- [Devoxx 2022](#devoxx-2022)
  - [Mon retour sur le devoxx 2022 à Parias](#mon-retour-sur-le-devoxx-2022-à-parias)
  - [Jour 1](#jour-1)
    - [Théories des catégories. Vous la connaissez déjà](#théories-des-catégories-vous-la-connaissez-déjà)
    - [Tester vos méthodes de refactoring sur la machine d'entrainement TCR](#tester-vos-méthodes-de-refactoring-sur-la-machine-dentrainement-tcr)
    - [Intégration a l'ère du Cloud avec Camel Quarkus](#intégration-a-lère-du-cloud-avec-camel-quarkus)
    - [Redonnez l'agilité à vos développeurs](#redonnez-lagilité-à-vos-développeurs)
    - [Reprenez le contrôle de votre Bash en devenant un Ninja de la CLI](#reprenez-le-contrôle-de-votre-bash-en-devenant-un-ninja-de-la-cli)
  - [Jour 2](#jour-2)
    - [Slow tech : Il est urgent de hacker le système](#slow-tech-il-est-urgent-de-hacker-le-système)
    - [Et si les microservices n'avaient rien à voir avec la technique](#et-si-les-microservices-navaient-rien-à-voir-avec-la-technique)
    - [Model Driven Design](#model-driven-design)
    - [Dois-je migrer en Réactive et comment ?](#dois-je-migrer-en-réactive-et-comment-)
    - [Micronaut AOT : Optimiser vos applications pour la JIT et GraalVM](#micronaut-aot-optimiser-vos-applications-pour-la-jit-et-graalvm)
    - [Continious Delivery on premise : Gerrit, Jenkins et Sonarqube entre dans un bar](#continious-delivery-on-premise-gerrit-jenkins-et-sonarqube-entre-dans-un-bar)
    - [S'affranchir de la pyramide de tests](#saffranchir-de-la-pyramide-de-tests)
    - [The unknown of Junit 5](#the-unknown-of-junit-5)
    - [Rex TDD et testContainers](#rex-tdd-et-testcontainers)
  - [Jour 3](#jour-3)
    - [Découper mon monolithe](#découper-mon-monolithe)
    - [Mob programming](#mob-programming)
    - [En quềte du clean code avec Sonar : 20 000 Lieues sous un océan de code](#en-quềte-du-clean-code-avec-sonar--20-000-lieues-sous-un-océan-de-code)
    - [400 endoits d'API et 2000 types : génèse ut utilisation du nouveau client Java pour ElasticSearch](#400-endoits-dapiet-2000-types-génèse-ut-utilisation-du-nouveau-client-java-pour-elasticsearch)
    - [Architecture microservices et cohérence des données : mais on fait comment pour de vrai ?](#architecture-microservices-et-cohérence-des-données--mais-on-fait-comment-pour-de-vrai-)

## Mon retour sur le devoxx 2022 à Parias

//todo 

## Jour 1

### Théories des catégories. Vous la connaissez déjà

Appliquer les théories mathématiques des **catégories** au développement logiciel.
Elle s'appuie sur la théorie des ensembles.
Objectifs :

Application -> Ensemble de services -> ensemble de fonctions.

Ces fonctions auraient un certain nombre de propriétés
* Composition de fonctions
* Distributivité ( On place les parenthèses où l'on veut : `h.(g.f) = (h.g).f`)

Ceci permet d’écrire un code plus souple. Qui pourrait être vue comme un ensemble de fonction simple.

Une catégorie :
* deux ensembles **E** et **F**
* des fonctions transformant des objets de **E** vers **F**
* Une fonction identité `id(x)=x`

Un **Monoïde** est une catégorie de **E** vers lui-même.
Un **monoïde** Contient un **élément neutre**.
On peut écrire un **monoïde** sous cette forme `{Ensemble, fonction ,Élement neutre}`.

Quelques exemples :
* `{Int, +, 0}`
* `{Int, *, 0}`
* `{String, *, ""}`
* `{List, add(), []}`

Pour généraliser on a également parlé de **Functor** et **Monade**, qui sont une application de la théorie des catégories à elle-même.
Elles permettent d'écrire du code plus générique, en manipulant des types génériques et des ensembles.
Une **Monade** est un **monoïde** à ce miveau.
Quelques exemples de **monades** :
* `{Stream<T>, map}`
* `{Optional<T>, map}`

Mon retour : Pour la culture, c'est intéressant. Je pense que la composition, on le fait naturellement. 
De même que l'abstraction.
Concernant la distributivité, effectivement ceci est moins naturel et on peut y voir un gain.
 Concernant les functor et monades, c'est utile quand on veut créer des libraires génériques.

### Tester vos méthodes de refactoring sur la machine d'entrainement TCR

Test && commit || revert

Méthodologie d'entrainement pour apprendre à tester/refactorer step by step
si ton teste plante => revert du code de production.

Danse ce lab, on exécutait un script, créé par las animateurs, qui avait ces fonctionnalités :
*. Quand on sauve, il lance les tests avec `./gradlew test`
*. Si le test passe : il commit.
*. Si le test échoue : les changements dans `src/main` sont annulés.

On devait coder deux katas connus : le bowwling et le rover sur mars.

Mon retour : cet outil est qu'il est à utiliser pour faire des katas. 
Pour avoir la méthodologie de refactoring en petites étapes (step by step). 
Mais je ne la pense pas appliquable pour le développement en entreprise. 
Pour moi, ceci est un outil d'apprentissage.


### Intégration a l'ère du Cloud avec Camel Quarkus

Présentation rapide de Camel. Permet de transférer / manipuler de flux d'une application à une autre. 
Fournit un petit DSL java pour cela.

Mon retour : Potentiellement utilise quand on a un grand nombre d'outils dont on veut pouvoir les faire communiquer ensemble. Ce qui n'est pas mon cas actuellement.


### Redonnez l'agilité à vos développeurs

Bien accompagner l'arrivée d'un développeur
Prendre son temps pour comprendre les problèmes.

// todo : voir la vidéo


### Reprenez le contrôle de votre Bash en devenant un Ninja de la CLI

Liste de différents qu'on peut installer dans le shell pour simplifier son application.

Mon retour : Pas mal d'outils qui semble utiles à tester.

## Jour 2

### Slow tech : Il est urgent de hacker le système

Dans 30 plus d'ordi si on continue ainsi.

Mitiger high tech avec slow tech.

Mon retour : //todo

### Et si les microservices n'avaient rien à voir avec la technique

Présentation de la loi De Conway.

_« Les organisations qui conçoivent des systèmes [...] tendent inévitablement à produire des designs qui sont des copies de la structure de communication de leur organisation. »_

Péesentation de 4 différents types d'équipes et de leurs communications
Une équipe :
* responsabilité claire
* possède un bout de logiciel

4 types d'équipes :
* **Stream align** : _you build it, you run it_.
* **Endling Team** : support pour l'équipe
* **Complicated suggestion** : apport une expertise spécifique
* **Plateform team** : Fournit des outils pour accélérer la livraison

3 type de communication :
* Collaboration
* Facilitation
* As a service

Mon retour : Très intéressant. On sous-estime l'impacte de la communication entreprise sur nos applications.
On remarque que beaucoup d'entreprise sont assez loin du système d'équipe et communications proposées. 
On peut se demander quel est l'impacte de nos structures d'entreprises sur nos produits. Mais on ne change pas facilement la structure d'une entreprise.

### Model Driven Design

Présentation intéressante pour ceux qui connaissaient déjà le DDD. Trop rapide pour les autres

Présentation de Deep Model et du Supple Design

Le **deep Model** est un modèle qui correspond fortement au métier.

**Breakthrough** Quand le développeur réussit à comprendre en profondeur le métier. Cette étape difficile à atteindre permet souvent une simplification importante du modèle tout en augmentant son expressivité.

**Supple design** est un ensemble de technique pour rendre le modèle solide et souple : 
* Séparation commande/query
* Immutabilité
* Assertions

Ateliers :
* Event storming
* Example mapping

Mon retour : La conférence était difficile à appréhender pour ceux qui ne connaissaient pas le DDD. 
Il y a eu un grand nombre de concepts sur lequel le présentateur est passé assez vite dessus. 
Le temps était trop court vis-a-vis de l'ambition du sujet. 
Les ateliers sont quant à eux intéressants et méritent sûrement qu'on y jette un œil.

### Dois-je migrer en Réactive et comment ?

La plus grande partie de cette conférence concernait sur une présentation de Spring reactor/webflux.

Il est conseillé d'utiliser la programmation réactive pour la scalabilité et non pour les performances

Il y a des pièges avec les bases de données relationnels qu'il faut connaître.

La programmation Réactive est un paradigme contaminant.

Mon retour : présentation technique de Spring reactor/webflux un peu trop poussée. 

### Micronaut AOT : Optimiser vos applications pour la JIT et GraalVM

Micronaut AOT est un concurrent à GraalVM.
Comment Micronaut permet d’optimiser son exécution par un grand nombre de traitements à la compilation
* Calcul de la réflexivité
* Transformation de yaml en Java
* Suppression de dépendances inutiles

Micronaut AOT permet quant à lui d'optimiser l'exécution sur la machine cible. C'est pour la prod et non pour le développeur.

Il va récupérer les infos de la machine cible. Infos qu'il peut calculer ou qu'on peut lui donner. 
A partir de là, il va virer tout ce qui est inutile.

Mon retour : Micronaut me semble être un concurrent directe à Quarkus. Je n'ai pas pu, par cette présentation voir la différence entre Quarkus et Micronaut pour faire un choix. Toutefois j'ai pu comprendre par cette présentation des mécanismes d'optimisations qu'utilise probablement Quarkus également. Il est également intéressant de connaitre les mécanismes utilisés pour optimiser un livrable pour la production.

### Continious Delivery on premise : Gerrit, Jenkins et Sonarqube entre dans un bar

Rex sur l'automatisation de la chaine de continious delivery.
commit ->  création PR -> build Jenkins -> Analyse Sonarqube.
Systeme de vote pour la PR
* Vote de Jenkins
* Vote de Sonarqube
* Vote manuel
Si vote positif -> Merge automatique -> Déploiement sur env de staging

Mon retour : Automatisation intéressante, mais non innovante pour ma part. 
C'est une guideline vers laquelle on peut tendre. Le système de 3 votes sur la PR est un système intéressant.

### S'affranchir de la pyramide de tests

La pyramide de test est-elle efficace ?
Retour d'expérience chez Doctolib.
La politique : faites des tests d'US. ils peuvent être UT, TI ou E22
Constat : 
* Les tests E2E sont moins cassant qu'avant
* les tests E2E peuvent être exécutés plus rapidement
  * 3 stratégies d'exécution :
    * mono thread
    * Massivement //
    * // Avec sélections
* les tests unitaires créent un contrat d'interfaces. Comment gérer un changement d'interfaces ?

![sketchnote pyramide](skechnotes/affranchir_pyramide_test.jpeg)ç

Mon retour : Sentiment mitigé. Des problématiques bien réelles qu'en teste met en place un contrat, même sur des tests à faible grain. 
Qu'un changement de ces contraintes provoquent un flou du point de vue refactoring est un réel problème qu'il faut appréhender. Ceci à un coût. 
Quant à la solution de préférer les tests End-to-end, j'ai des doutes. 
Il est toujours bon de savoir remettre un dogme, tels que la pyramide de tests, pour savoir si cette méthodologie est toujours vrai ou bien applicable à mon cas.

### The unknown of Junit 5

Explication rapide des nouvelles fonctionnalités de Juint5
* Tests paramétrés
* nommage des tests
* Parallélisation 
* Création des Extensions

Mon retour : Pourquoi j'utilise encore Junit4 ?

### Rex TDD et testContainers

Comment utiliser testContainer dans un contexte Java. 
En particulier sur des applications qui utilisent un certain nombre d'outils extérieurs tels que des Bdd, RabbitMQ, Kafka etc.

On peut dans ce cas écrire des tests unitaires où l'on doit un peu tout mocker semblent bien vide. 
Dans certains cas, des tests intégration avec la bdd ou l'outil de messaging peut s'avérer plus pertinent à mettre en place. $$ais comment mettre en place des tests simple et solides dans ce cas ? TestContainer est là pour vous.

TestContainer va s'occuper de :
* télécharger l'image docker contenant vos outils
* initialiser le conteneur
* le test attend que le conteneur soit prêt.
* on vide le conteneur à la fin du test afin de s'assurer que nos tests soient idempotent.

Mon retour : Cette présentation n'a pas vraiment parler de TDD mais juste de la mise en place de TestConainer. 
Dans certains contextes le grain tests unitaire est un grain trop faible. 
TestContainer semble une solution intéressante pour mettre en place des tests unitaire avec des outils tierce simple et solide.

## Jour 3

### Découper mon monolithe

Trouver les différents domaines
Savoir en base quelles tables/champs appartiennent à quel domaine
Ajouter une fonctionnalité a coté du monolithe.
Découvertes des bubble contextes. Comment ils communiquent ?
* Par BDD (A Éviter)
* Par query d'API
* Par Commande d'API
* Par flux d'état
* Par Évènements
* Par notifications + Commande d'api

Mon retour : atelier intéressant et difficile.
Splitter un monolithe ce n'est pas simple. 
Présentation d'ateliers pour aider. 
Toutefois, ce fut frustrant, car on n'a pas vraiment "splitter un monolithe", on a ajouté de nouvelles fonctionnalités à côté du monolithe en modifiant à minimum celui-ci. 
Finalement en travaillant de cette manière le monolithe se vide petit à petit. Mais c'est un processus très lent. 

### Mob programming

![sketchnote mob programming](skechnotes/mobProgramming.jpeg)

### En quềte du clean code avec Sonar : 20 000 Lieues sous un océan de code


Présentation des différents sonar* (qube/cloud/lint).


Mon retour : Je n'ai pas appris grand-chose. Sonar tente de voir plus large et s'orient vers le clean code.
Considère de regarder le nouveau code.
Corriger au plus prêt de la source et donc utiliser sonarlint puis au commit

### 400 endoits d'API et 2000 types : génèse ut utilisation du nouveau client Java pour ElasticSearch

Réflexion sur une API très complexe pour simplifier son utilisation.
Écriture d'un nouveau client plus intuitif dans lequel on peut utiliser la puissance d'autocompletion des IDE.
Règles :
* On ne veut pas que l'utilisateur ait à deviner un nom de classe
* On ne veut pas que l'utilisateur ait des imports (hors ceux de base) à faire
* On veut avoir une correspondance forte entre le code java et json.

Pour cela, ils ont eut l'idée d’utiliser les lambdas et le pattern Builder.

Mon retour : Plus qu'apprendre à utiliser ce client, la méthologie est intéressante et peut probablement être utilisés pour de nombreux client REST.

### Architecture microservices et cohérence des données : mais on fait comment pour de vrai ?

Maintenir la cohérence des données dans un contexte distribue est un challenge en soi. 
Finit les transactions ACID. Il va falloir composer.
Il va falloir réfléchir en termes de transactions distribuées.

Cette présentation décrit deux méthodes :
* SAGA
* LRA (Long Running Action)

Mon retour : Présentation complexe pour un sujet complexe, mais tout aussi important voir vitale.
Une architecture non monolithe amène forcément le problême de la cohérence des données. Sujet souvent sous-estimé.

slides : https://www.youtube.com/watch?v=7HC6ZfSy8M4&t=335s