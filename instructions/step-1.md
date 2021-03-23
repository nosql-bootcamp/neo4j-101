## Prise en main

Une fois la base de données lancée, ouvrez la page [http://localhost:7474/browser/](http://localhost:7474/browser/) dans un browser. Connectez-vous au serveur avec l'utilisateur `neo4j` et le mot de passe renseigné lors de l'installation (par défaut le mot de passe est `neo4j`)

Une fois authentifié, pour découvrir les concepts de base, tapez la commande suivante :

```
:play concepts
```

Pour découvrir le langage Cypher, tapez la commande suivante :

```
:play cypher
```

Quelques exercices complémentaires (basées sur les données créées dans l'exercice de découverte de **Cypher** ci-dessus) :

* Vous pouvez écrire une requête qui renvoie les prénoms des personnes
* Vous pouvez écrire une requête qui envoie l'ensemble des noeuds qui sont à une distance de 4 du noeud *"Emil"*

Pour aller plus loin sur les possibilités de requêtes de Cypher, vous pouvez regarder en détail la clause [MATCH](https://neo4j.com/docs/developer-manual/3.3/cypher/clauses/match/) ainsi que les [fonctions disponibles](https://neo4j.com/docs/developer-manual/3.3/cypher/functions/).

Si il vous reste un peu de temps, tapez la commande suivante :

```
:play northwind graph
```

Solutions : 

* Requête qui renvoie les prénoms des personnes : `MATCH (x) RETURN x.name`
* Requête qui envoie l'ensemble des noeuds qui sont à une distance de 4 du noeud *"Emil"* : `MATCH (x:Person)-[:KNOWS *4]->(y:Person) WHERE x.name = 'Emil' RETURN y`
