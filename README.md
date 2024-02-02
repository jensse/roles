# Roles

The roles defiend here have a stake in the case-information registered by the norwegian courts.  The Roles are observed from whitin the case, looking out.

A list of national registers know to the norwegian press can be found here: https://presse.no/offentlighet/register/alle-registre/

## PMATCH (n:Kilder) poulate neo4j

If you wish to use this roles in neo4j, they may be loaded with the following command from browser.  **Important: No whitespace in header**


```cypher

LOAD CSV WITH HEADERS FROM 'https://raw.githubusercontent.com/dahe5/roles/master/court_no.csv' AS line
CREATE (:Role { name: line.name })

```

```cypher

MATCH (n:Kilder) DETACH DELETE n
LOAD CSV WITH HEADERS FROM
'https://raw.githubusercontent.com/dahe5/roles/master/kilder.csv' AS line FIELDTERMINATOR ';'
CREATE (:Kilder { name: line.name, description: line.description })

```
