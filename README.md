# neo4j-101

**Neo4j 101** est un workshop permettant de découvrir la base de données NoSQL Neo4J et son écosystème, étape par étape.

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a>

## Introduction
Neo4J est une base de données orientée graphes créée en 2007 par la société	**Neo Technology**. À la différence d'une base de données SQL, les relations (jointures en SQL) sont optimisées. De fait, les opérations mettant en oeuvre des relations garantissent des performances linéaires. Les bases de données SQL présentent des performances qui se dégradent exponentiellement lors des jointures. En ce qui concerne les autres types de bases NoSQL (orientées KV, orientées colonnes, orientées documents), elles ne proposent tout simplement pas de jointures.

Neo4J fait partie des rares bases NoSQL qui offre des propriétés ACID.

Neo4J s'appuie sur le langage Cypher, déclaratif, comme le langage SQL. Ce langage propose nativement des fonctionnalités d'algorithmique des graphes telles que le calcul de plus court chemin.

Le manuel de développement est [disponible ici](http://neo4j.com/docs/developer-manual/3.0/).

## Use Cases
Voici quelques use cases pour lesquels les bases de données orientées graphes sont de solutions adaptées :

* Système de recommandations
* Réseaux (sociaux ou non)
* Gestion des données de référence
* Détection de fraude
* Recherche sémantique

## Neo4J et le CAP theorem
Un graphe Neo4J ne peut pas être partitionné. Il est possible d'installer une base Neo4J sur plusieurs serveurs pour mettre en oeuvre un service hautement disponible mais **chaque noeud dispose de l'ensemble des données du cluster**. L'écriture est effectuée sur la base d'un principe de master/slaves, le master maintient des réplicats à jour. Si le noeud master tombe en panne, un nouveau master est élu parmi les noeuds slaves synchrones. Les opérations d'écriture ainsi que l'élection d'un master s'appuient sur un principe de **quorum**.

## Installation
Pour installer Neo4J, rendez-vous sur le [lien suivant](https://neo4j.com/download/community-edition/), téléchargez la version adaptée à votre OS et suivez les instructions d'installation.

## Prise en main
Une fois la base de données lancée, ouvrez la page [http://localhost:7474/browser/](http://localhost:7474/browser/) dans un browser. Connectez-vous au serveur, le **login/mot de passe** par défaut est **neo4j/neo4j**.

Une fois authentifié, pour découvrir les concepts de base, tapez la commande suivante :

```
:play concepts
```

Pour découvrir le langage Cypher, tapez la commande suivante :

```
:play cypher
```

Quelques exercices complémentaires (basées sur les données créées dans l'exercice de découverte de Cypher ci-dessus) :

* Vous pouvez écrire une requête qui renvoie les prénoms des personnes
* Vous pouvez écrire une requête qui envoie l'ensemble des noeuds qui sont à une distance de 4 du noeud *"Emil"* ?

Une refcard sur le langage Cypher est [disponible ici](https://neo4j.com/docs/cypher-refcard/current/).
Pour aller plus loin sur les possibilités de requêtes de Cypher, vous pouvez regarder en détail la clause [MATCH](http://neo4j.com/docs/developer-manual/3.0/cypher/#query-match) ainsi que les [fonctions disponibles](http://neo4j.com/docs/developer-manual/3.0/cypher/#query-function).

Si il vous reste un peu de temps, tapez la commande suivante :

```
:play movie graph
```
