# Roles

The roles defiend here have a stake in the case-information registered by the norwegian courts.  The Roles are observed from whitin the case, looking out.


## Populate neo4j

If you wish to use this roles in neo4j, they may be loaded with the following command from browser.

```cypher

   LOAD CSV WITH HEADERS FROM 'https://raw.githubusercontent.com/dahe5/roles/master/court_no.csv' AS line
   CREATE (:Role { name: line.name })

```

```cypher

   LOAD CSV WITH HEADERS FROM
   'https://raw.githubusercontent.com/dahe5/roles/master/kilder.csv' AS line FIELDTERMINATOR ';' CREATE (:Role { name: line.name , line.description})
```

# Heading

## Heading 2
