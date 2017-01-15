## Installation

Pour télécharger **Neo4J**, rendez-vous sur le [lien suivant](https://neo4j.com/download/community-edition/), téléchargez la version `tar` ou `zip` adaptée à votre OS.

Suivez ensuite les instructions d'installation.

Par exemple pour l'installation sous Unix / MacOS :

* Dézippez l'archive dans le dossier de votre choix, par exemple `~/progs/neo4j-community-3.1.0`.
* Démarrez Neo4j :
```bash
cd ~/progs/neo4j-community-3.1.0
bin/neo4j console
```
* Ouvrez un navigateur à l'adresse suivante : http://localhost:7474/
* Changez le mot de passe du compte neo4j

## Données

Neo4j stocke par défaut ses données dans le répertoire `data/databases/graph.db` du répertoire d'installation.

Ce répertoire contient l'ensemble des données du graphe. Il n'existe pas de notion de schéma dans Neo4J, pour créer plusieurs graphes, il faut démarrer plusieurs instances de Neo4J pointant sur plusieurs répertoires différents.

Pour cela, il faut modifier la configuration se trouvant dans le fichier `conf/neo4j.conf`, en particulier les propriétés suivantes :

```
# The name of the database to mount
dbms.active_database=graph.db

# Paths of directories in the installation.
dbms.directories.data=data
```

## Next

Vous pouvez passer à l'étape suivante : [Prise en main](./step-1.md)
