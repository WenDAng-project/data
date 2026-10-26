# WRITE dataset
This repository contains the RDF dataset developed within **WenDAng - WRITE digital archive** project.
The dataset connects artworks, their calligraphic or writing-like components, artists, and their contexts, supporting comparison, quantitative analysis, and the identification of recurrent patterns. It forms part of the wider WenDAng semantic infrastructure together with the WRITE ontology and thesaurus. 

## Persistent identifiers and URI policy
The WRITE dataset is identified by the persistent URI:  
`https://w3id.org/write/data/`  

Individual dataset records are identified using the following URI pattern:  
`https://w3id.org/write/data/item/{id}`

## Format
The WRITE dataset is an RDF dataset and it serialised in Turtle (.ttl) format.

## Used vocabularies
The WRITE dataset is primarily structured using the [WRITE ontology](https://w3id.org/write/ontology), which combines domain-specific classes and properties with selected elements reused from Wikidata. The [WRITE thesaurus](https://w3id.org/write/thesaurus) provides controlled terminology for describing culturally specific concepts.  
Further details about the vocabularies used in the dataset are provided in its VoID description.

## Dataset description
A machine-readable description of the WRITE dataset is provided using **VoID (Vocabulary of Interlinked Datasets)**. It includes information about the dataset scope, access points, URI structure, vocabularies used, licence, provenance, and contributor roles.  
**https://wendang-project.github.io/data/void.ttl**

## SPARQL query example
The WRITE data can be queried using SPARQL. The following example query examines the frequency of different script styles among Chinese-language “Calli-Writing” units.  

```sparql
PREFIX ns1: <https://w3id.org/write/ontology#>
PREFIX ns2: <http://www.wikidata.org/prop/>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

SELECT ?scriptStyle (COUNT(DISTINCT ?unit) AS ?count)
WHERE {
    ?unit a ns1:CalliWritingUnit ;
          ns2:P407 <https://www.wikidata.org/entity/Q7850> ;
          ns2:P9302 ?style .

    ?style rdfs:label ?scriptStyle .
}
GROUP BY ?scriptStyle
ORDER BY DESC(?count)
```

### Contact
Katarina Lučić - PhD candidate  
Department of Interpreting and Translation, University of Bologna (Italy)    
📧 katarina.lucic2@unibo.it

### License
This work is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
