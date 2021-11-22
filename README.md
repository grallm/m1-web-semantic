# Semantic Web - Car crash in "Loire-Atlantique"

## Description
A Semantic Web project for our first year of Software Architecure Master at the University of Nantes.

After finding an interesting dataset we have to transform it in a usable linked data format (Turtle). By hosting it on Apache Jena Fuseki we are able to request the data with SPARQL.

We will also be able to link our data with the other crouse groups and host our Jena server in a Docker container on Google Cloud Platform.

## Used dataset
[Interventions pour accident sur la voie publique en Loire-Atlantique](https://data.loire-atlantique.fr/explore/dataset/284400017_interventions-pour-accident-sur-la-voie-publique-en-loire-atlantique/)

## From CSV to Turtle
By using the mapping files `mapping-crashes.sparql` and `mapping-locations.sparql` with Tarql we have been able to transform the CSV data to a Turtle Linked Data.

```
./tarql projet-sem/mapping/mapping-crashes.sparql projet-sem/data/accidents.csv > projet-sem/mapping/data-accidents-mag.ttl
./tarql-1.2/bin/tarql projet-sem/mapping/mapping-locations.sparql projet-sem/data/accidents.csv >> projet-sem/mapping/data-accidents-mag.ttl
```

## Ontologies
To help us convert our RDF Turtle to OWL we used [this website](https://www.ldf.fi/service/owl-converter/)

## Project members
- Malo GRALL
- Guillaume POIGNANT
- Amar TIOUS

## Used technologies
- RDF Schemas
- Linked Data
- SPARQL
- Apache Jena
- Docker
- Tarql