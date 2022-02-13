## Installation

### Installation dans le cloud

Plutôt que d'installer Neo4J localement, vous pouvez profiter de la version cloud qui est accessible [https://neo4j.com/cloud/aura/?ref=get-started-dropdown-cta](ici) (bouton bleu `Start free` au milieu de la page).

**Pensez à bien enregistrer votre mot de passe, il ne vous est donné qu'une seule fois.**

Cette option est plus simple du point de vue de l'installation, néanmoins il vous faudra adapter vos requêtes pour la suite.


### Installation en local

Pour télécharger **Neo4J**, rendez-vous sur le [lien suivant](https://neo4j.com/download-center/#releases), téléchargez la version **Community server** `tar` ou `zip` de adaptée à votre OS.

Suivez ensuite les instructions d'installation.

Par exemple pour l'installation sous Unix / MacOS :

* Dézippez l'archive dans le dossier de votre choix, par exemple `~/progs/neo4j-community-3.5.14`.
* Démarrez Neo4j :
```bash
cd ~/progs/neo4j-community-3.5.14
bin/neo4j console
```
* Ouvrez un navigateur à l'adresse suivante : http://localhost:7474/
* Le compte utilisateur qui a été créé par défaut est `neo4j` avec le mot de passe `neo4j`
* Changez le mot de passe du compte `neo4j`

## Données

Neo4j stocke par défaut ses données dans le répertoire `data/databases/graph.db` du répertoire d'installation.

Ce répertoire contient l'ensemble des données du graphe. Il n'existe pas de notion de schéma dans Neo4J ! Pour créer plusieurs graphes, il faut démarrer plusieurs instances de Neo4J pointant sur plusieurs répertoires différents.

Pour cela, il faut modifier la configuration se trouvant dans le fichier `conf/neo4j.conf`, en particulier les propriétés suivantes :

```
# The name of the database to mount
dbms.active_database=graph.db

# Paths of directories in the installation.
dbms.directories.data=data
```

## Next

Vous pouvez passer à l'étape suivante : [Prise en main](./step-1.md)
