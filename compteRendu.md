# Devoxx 20222

- [Devoxx 20222](#devoxx-20222)
  - [Jour 1](#jour-1)
    - [Théories des catégories. Vous la connaissez déja](#théories-des-catégories-vous-la-connaissez-déja)
    - [Tester vos méthodes de refactoring sur la machine d'entrainement TCR](#tester-vos-méthodes-de-refactoring-sur-la-machine-dentrainement-tcr)
    - [Intégration a l'ère du Cloud avec Camel Quarkus](#intégration-a-lère-du-cloud-avec-camel-quarkus)
    - [Redonnez l'agilité à vos dévoloppeurs](#redonnez-lagilité-à-vos-dévoloppeurs)
    - [Reprenez le contrôle de votre Bash en devenant un Ninja de la CLI](#reprenez-le-contrôle-de-votre-bash-en-devenant-un-ninja-de-la-cli)
  - [Jour 2](#jour-2)
    - [Slow tech : Il est urgent de hacker le système](#slow-tech-il-est-urgent-de-hacker-le-système)
    - [Et si les microservices n'avaient rien à voir avec la technique](#et-si-les-microservices-navaient-rien-à-voir-avec-la-technique)
    - [Model Driven Design](#model-driven-design)
    - [Dois-je migrer en Reactive et comment ?](#dois-je-migrer-en-reactive-et-comment-)
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

## Jour 1

### Théories des catégories. Vous la connaissez déja

Appliquer les théories mathématiques des **catégories** au développement logiciel.
Elle s'appuie sur la théories des ensembles.
Objectif:

Application ->  Ensemble de services -> ensemble de fonctions.

Ces fonctions auraient un certain nombre de propriétés
* Composition de fonctions
* Distributivité (On place les parentheses où l'on veut : `h.(g.f) = (h.g).f`

Ceci permet d’écrire une code plus souple. Qui pourrait être vue comme un ensemble de fonction simple.

Une catégorie :
* deux ensemble **E** et **F**
* des fonction transformant des objets de **E** vers **F**
* Une fonction identitée `id(x)=x`

Un **Monoïde** est une catégorie de **E** vers lui-même.
Un **monoîde** Contient une **élément neutre**.
On peut écrire un **monoîde** sous cette forme `{Ensemble, fonction ,Élement neutre}`.

Quelques exemples :
* `{Int, +, 0}`
* `{Int, *, 0}`
* `{String, *, ""}`
* `{List, add(), []}`

Pour généraliser on a également parlé de **Functor** et **Monade**. qui sont une peut des application des théories de catégories à elle-même.
Elles permèttent d'écrire du code plus générique, en manipulant des types générique et des ensembles.
Une **Monade** est un **monoïde** à ce miveau.
Quelques exemples de **monades** :
* `{Stream<T>, map}`
* `{Optional<T>, map}`

Mon retour : Pour la culture, c'est intéressante. Je pensqe que la composition, on le fait naturellement. de même que l'abstraction. Concernante la distributivité, effectivement ceci est moins naturel et on peux y voir un gain. Concernant les functor et monades, c'est utiles quand on veut créer des libraires génériques. 

### Tester vos méthodes de refactoring sur la machine d'entrainement TCR

Test && commit || revert

Méthodologiet d'entrainement pour apprendre a tester/refactorer step by step
si ton teste plante => revert du code de production.

Danse ce labs, on lançait un script créé par las animateurs qui avait ces fonctionnalités :
*. Quand on sauve, il lance les tests avec `./gradlew test`
*. Si le seste passe : il commit.
*. si le test échoue : les changements dans `src/main` sont annulés.

On devait coder deux katas connues : lo bowwling et le rover sur mars.

Mon retour :  cet outil est qu'il est à utiliser pour faire des katas. pour avoir la méthodlogie de refactoring en petites étapes (step by step). Mais je ne je pense pas applqiuable pour le développement en entreprise. Pour moi, ceci est un outil d'apprentissae au développement avec refactoring continue.


### Intégration a l'ère du Cloud avec Camel Quarkus

Présentation rapide de Camel. Perment de transférer / manipuler de flux d'une application à une autre. 
Fournit un petit DSL java pour cela.

Mon retour : Potentiellement utilse quand on à un grand nombre d'outil dont on veut pouvoir les faire communiquer ensemble. Ce qui n'est pas mon cas actuellement.


### Redonnez l'agilité à vos dévoloppeurs

Bien accompagner l'arrivée d'un développeur
Prendre son temps pour comprendre les problèmes.

// todo : voir la vidée


### Reprenez le contrôle de votre Bash en devenant un Ninja de la CLI

Liste de différents qu'on peut installer dans le shell pour simplifier son application.

mon retour : Pas mal d'outils qui semble utilese à tester.

## Jour 2

### Slow tech : Il est urgent de hacker le système

dans 30 plus d'ordi si on continue ainsi.

Mitiger high tech avec slow tech.

mon retour : //todo

### Et si les microservices n'avaient rien à voir avec la technique

Présentation de la loi De Conway.

_« les organisations qui conçoivent des systèmes [...] tendent inévitablement à produire des designs qui sont des copies de la structure de communication de leur organisation. »_

Presentation de 4 différents types d'équipes et de leurs communications
Une équipe :
* responsabilité claire
* possède un bout de logiciel

4 types d'équipes :
* **Stream align** : _you build it, you run it_.
* **Endling Team** : support pour l'équipe
* **Complicated suggestion** : apport une expertise spécificique
* **Plateform team** : Fournit des outils pour accélérer la livraision

3 type de communication :
* Collaboration
* Facilitation
* As a service

Mon retour : Très intéressant. On sous-estime l'impacte de la communication entreprise sur nos applications. On remarque que beaucoup d'entreprise sont assez loins du systềme d'équipe et communication proposés. On peut se demander quel est l'impacte de nos structures d'entreprises sur nos produits. Mais on ne change pas facilement la structure d'une entreprise. 

### Model Driven Design

Présentation intéressante pour ceux qui connaissait déjà le DDD. Trop rapide pour les autres

Présentation de Deep Model et du Supple Design

Le **deep Model** est un modèle qui correspond fortement au métier.

**Breakthrough** Quand le développeur réussit à comprendre en profondeur le métier. Cette étape difficile à atteindre permet souvent une simplification importante du modèle tout en augmentant son expressivité.

**Supple design** est un ensemble de technique pour rendre le modèle solide et souple : 
* Séparation commande/query
* Immutablité
* Assertions

Ateliers :
* Event storming
* Example mapping

Mon retour : La conférence était difficile a appréhender pour ceux qui ne connaissais pas le DDD. Il y a eu un grand nombre de concepts sur lequel le présentateur est passé assez vite dessus. Le temps était trop court vis a vis de l'ambition du sujet. Les ateliers sont quand à eux intéressants et méritent sûrement qu'on y jette un œil.

### Dois-je migrer en Reactive et comment ?

La plus grande parties de cette conférence concernait sur une présentation de Spring reactor/webflux.

Il est conseillé d'utilisé la programmation réactive pour la scalibité et non pour les performances

Il y a des pièges avec les bases de données relationnels qu'il faut connaître.

La programmation Reactive est un paradigme contaminant.

Mon retour : présentation technique de Spring réactor/webflux un peu trop poussés. 

### Micronaut AOT : Optimiser vos applications pour la JIT et GraalVM

Micronaut AOT est un concurrent à GraalVM.
Comment Micronaut permet d’optimiser son execution par un grand nombre de traitement à la compilation
* Calcul de la réflexivité
* Transformation de yaml en Java
* Suppression de dépendances inutiles

Micronaut AOT permet quand à lui d'optimiser l'éxécution sur la machine cible. C'est pour la prod et non pour le dévolopeur.

Il va récupérer les infos de la machine cible. Infos qu'il peut calculer ou qu'on peut lui donner. A partir de là , il va virer tout ce qui est inutile.

Mon retour : Micronaut me semble être un concurrent dirècte à Quarkus. Je n'ai pas pu, par cette présentation voir la différence entre Quarkus et Micronaut pour faire un choix. Toutefois j'ai pu comprendre par cette présentation des mécanismes d'optimisations qu'utilise probablement Quarkus également. Il est également intéressant de connaitre les mécanismes utilisés pour optimiser un livrable pour la production.

### Continious Delivery on premise : Gerrit, Jenkins et Sonarqube entre dans un bar

Rex sur l'automatisation de la chaine de condinious delivery.
commit ->  création PR -> build Jenkins -> Analyse Sonarqube.
Systeme de vote pour la PR
* Vote de Jenkins
* Vote de Sonarqube
* Vote manuel
Si vote positif -> Merge automatique -> Deploiement sur env de staging

mon retour : Automatisation intéressante mais non inovante pour ma part. C'est une guideline vers laquelle on peut tendre. Le système de 3 votes sur la PR est un système intéressant.

### S'affranchir de la pyramide de tests

La pyramide de test est-elle efficace ?
Retour d'expérience chez Doctolib.
La politique : faites des tests de US. il peuvent être UT, TI ou E22
Constat : 
* Les tests E2E sont moins cassant qu'avant
* les tests E2E peuvent être exécutés plus rapidement
  * 3 statégies d'exécution :
    * mono thread
    * Massivement //
    * // Avec sélactions
* les tests unitaires créent un contrat d'interfaces. Comment gérer un changement d'interfaces ?

![sketchnote pyramide](skechnotes/affranchir_pyramide_test.jpeg)ç

Mon retour : Sentiment mitigé. Des problématiques bien réelles qu'en teste met en place un contrat, même sur des tests à faible grain. Qu'un changement de ces contrait provoque un flou du point de vue refactoring est un réel problème qu'il faut appréhenter. Ceci à un coût. Quand à la solution de préférez les tests End-to-end, j'ai des doutes. Il est toujours bon de savoir remettre un dogme, tels que la pyramide de tests, pour savoir si cette méthodologie est toujours vrai ou bien appliquable à mon cas. 

### The unknown of Junit 5

Explications rapide des nouvelles fonctionnalités de Juint5
* Tests parametrés
* nommage des tests
* Parallèlisation 
* Creation des Extensions

Mon retour : Pourquoi j'utilise encore junit 4 ?

### Rex TDD et testContainers

Comment utiliser testContainer dans un contexte Java. On particulier sur des application qui utilisent un certain nombre d'outils extéreurs tels que des Bdd, RabbitMQ, Kafka etc.

On peut dans ce cas écrire des tests unitaires où l'on doit un peut tout manquer semblent bien vide. Dans certaint cas, des tests intégration avec la bdd ou l'outil de messaging peut s'avérer plus pertinant à mettre en place. mais comment mettre en place des tests simple et solides dans ce cas ? TestContainer est la pour vous.

TestContainer va s'occuper de :
* télécharger l'image docker contenant vos outils
* initialiser le conteneur
* le tests attent que le conteneur est prêt.
* on vide le conteneur à la fin du tests àfin de s'assurer que nos tests soient idempotent.

mon retour : Cette présentation n'a pas vraiment parler de TDD mais juste de la mise en place de TestConainer. Dans certaint contexts le grain tests unitaire est un grain trop faible. TestContainer semble une solution intéressante pour mettre en place des tests unitaire avec des outils tierce simple et solide.

## Jour 3

### Découper mon monolithe

Trouver les différents domaines
Savoir en base quelles tables/champs appartiennent à quel domaine
Ajouter une foncitonnalité a coté du monolythe.
Découvertes des bubble contextes. Comment ils communiques ?
* par BDD (A Éviter)
* Par query d'API
* Par Commande d'API
* Par flux d'état
* Par Évènements
* Par notifications + Commande d'api

Mon retour : atelier intéressant et difficile. Splitter un monolithe ce n'est pas simple. Présentation d'ateliers pour aider. Toutefois ce fut frustrant car on n'a pas vraiment "splitter un monolithe", on à ajouté de nouvelles fonctionnalités à coté du monnolithe en modifiant à minimum celui-ci. Au final en travaillant de cette manière le monolithe se vide petit à petit. Mais c'est un processus très lent. 

### Mob programming

![sketchnote mob programming](skechnotes/mobProgramming.jpeg)

### En quềte du clean code avec Sonar : 20 000 Lieues sous un océan de code


Présentation des différents sonar* (qube/cloud/lint).


Mon retour : Je n'ai pas appris grand chose. Sonar tente de voir plus large et s'orient vers le clean code.
Considère de regarder le nouveau code.
Corriger au plus prèt de la sources et donc utiliser sonarlint puis au commit

### 400 endoits d'API et 2000 types : génèse ut utilisation du nouveau client Java pour ElasticSearch

Reflection sur une API très complexe pour simplifier sont utilisation.
Écriture d'une nouveau client plus intuitif dans lequel on peut utiliser la puissance d'autocompletion des IDE.
Règles :
* On ne veut pas que l'utilisateur ait a Deviner un nom de classe
* On ne veut pas que l'utilisateur ait des imports (hors ceux de base) à faire
* On veut avoir une correspondance forte entre le code java et json.

Pour celà ils ont eut l'idée d’utilser les lambdas et le pattern Builder.

Mon retour : Plus qu'apprendre à utiliser ce client, la méthologie est intéressante et peut probablement être utilisés pour de nombreux client REST.

### Architecture microservices et cohérence des données : mais on fait comment pour de vrai ?

Maintenir la cohérence des données dans un contexte distribue est un challenge en soit. Finis les transcation ACID. il va falloir composer.
Il va falloir réfléchire en terme de transaciton distribuées.

Cette présentation décrit deux méthodes :
* SAGA
* LRA (Long Running Action)

Mon retour. Présentation complexe pour un sujet complexe mais tout aussi important voir vitale. Une architecture non monolithe amène forcement le prèblèle de la cohérence des données. Sujet souvent sous-estimés.