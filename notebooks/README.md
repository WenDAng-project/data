
# WRITE Dataset — Data Processing Notebooks

This directory contains the Jupyter notebooks used to clean, harmonise, transform, and enrich the WRITE RDF dataset, developed within the **WenDAng – WRITE Digital Archive project**.  
The notebooks document different stages of data preparation, using both JSON-LD and Turtle serialisations.

## Notebooks

| Notebook | Description |
|---|---|
| `data_cleaning.ipynb` | Cleans data exported from Omeka S. |
| `ontology_alignment.ipynb` | Aligns dataset properties with the WRITE Ontology. |
| `remove_keys.ipynb` | Removes unnecessary keys. |
| `boolean_conversion.ipynb` | Converts selected values into booleans. |
| `thesaurus_alignment.ipynb` | Aligns dataset values with the WRITE Thesaurus. |
| `inverse_relations.ipynb` | Generates additional (inverse) RDF relationships. |
| `related_CWUs.ipynb` | Generates relationships between Calli-Writing units. |
| `accuracy_annotations.ipynb` | Adds RDF-star annotations for approximate values. |
| `VIAF_ULAN_mapping.ipynb` | Enriches person resources with VIAF and ULAN identifiers. |
| `geographical_enrichment.ipynb` | Enriches location resources with geographical coordinates from Wikidata. |

## Usage

The notebooks document different stages of data processing and are not intended as a fully automated pipeline. Some require intermediate datasets, additional input files, Python libraries, or access to external services.  
File paths and dependencies may need to be adapted before execution.

