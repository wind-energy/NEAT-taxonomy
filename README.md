# Wind energy taxonomy of topics

Controlled vocabularies such as taxonomies allow an accurate and controlled approach in describing datasets. One of such controlled vocabulary is Wind Energy Taxonomy of Topics. This taxonomy is the result of EERA JP WIND IRPWind Open Data initiative that took place in 2017 in which wind energy experts generated the first version of the taxonomy as an input for defining and structuring [wind energy metadata](https://zenodo.org/record/4013191).

The report of this work is available at Zenodo: https://www.zenodo.org/record/1199489#.XSD6haeQ3RY

In 2018, the taxonomy of topics was improved during the internal project of DTU Wind Energy titled 'FAIR Digitalization':
https://www.zenodo.org/record/1493874#.XSD7TaeQ3RY

In 2020, the definition of taxonomy terms were added and the taxonomy was converted into FAIR machine-actionable controlled vocabulary using [sheet2rdf](https://github.com/fair-data-collective/sheet2rdf).  The controlled vocabulary is served to humans and machines using an instace of [OntoStack](http://data.windenergy.dtu.dk/ontologies/view/) hosted by DTU Wind Energy.


# Tooling
## [sheet2rdf](https://github.com/fair-data-collective/sheet2rdf)

This repository hosts automatic workflow, executed by means of Github actions, and underlying shell and python scripts which:

- Fetches Google Sheet, containing the taxonomy terms and their defitions, from Google Drive and stores is at `xlsx` and `csv` files
- Converts fetched sheet to machine-actionable and FAIR RDF vocabulary using [xls2rdf](https://github.com/sparna-git/xls2rdf)
- Tests the resulting RDF vocabulary using [qSKOS](https://github.com/cmader/qSKOS/)
- Commits conversion results and tests logs to this repository
- and deploy RDF vocabulary to OntoStack to be served to humans and machines

This workflow is an extension of [excel2rdf](https://github.com/fair-data-collective/excel2rdf-template).

## [OntoStack](http://data.windenergy.dtu.dk/ontologies/view/)

OntoStack is a set of orchestrated micro-services configured and interfaced such that they can intake vocabularies and resolve their terms and RDF properties upon requests either by humans or machines.

Some of OntoStack micro-services are:

- [Jena Fuseki](https://jena.apache.org/documentation/fuseki2/) a graph database
- [SKOSMOS](http://www.skosmos.org/) a web-based SKOS browser acting as a front-end for the vocabularies persisted by the graph database
- [Træfik](https://doc.traefik.io/traefik/) an edge router responsible for proper serving of URL requests

# Taxonomy implementation
The taxonomy is implemented in:
- [DTU Data](https://data.dtu.dk/DTU_Wind_Energy)
- [CEDAR](cedar.metadatacenter.org/) through integration with [BioPortal](https://bioportal.bioontology.org/ontologies/WETAXTOPICS/)
- ~~[ShareWind](https://sharewind.eu/)~~

# Contribute

The taxonomy is intended to be used and further developed by the community. Therefore, we welcome collaborators willing to take part in the further development of the taxonomy. If you are one of them either request to become one of the taxonomy admin and/or post GitHub issues.