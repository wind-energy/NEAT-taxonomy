# Wind energy taxonomy of topics

Controlled vocabularies such as taxonomies allow an accurate and controlled approach in describing datasets. One of such controlled vocabulary is Wind Energy Taxonomy of Topics. This taxonomy is the result of EERA JP WIND IRPWind Open Data initiative that took place in 2017 in which wind energy experts generated the first version of the taxonomy as an input for defining and structuring [wind energy metadata](https://zenodo.org/record/4013191).

The report of this work is available at Zenodo: https://www.zenodo.org/record/1199489#.XSD6haeQ3RY

In 2018, the taxonomy of topics was improved during the internal project of DTU Wind Energy titled 'FAIR Digitalization':
https://www.zenodo.org/record/1493874#.XSD7TaeQ3RY

In 2020, the definition of taxonomy terms were added and the taxonomy was turn into FAIR and machine-actionable form, served to humans and machines using DTU Wind Energy OntoStack: http://data.windenergy.dtu.dk/ontologies/view/

Currently, the taxonomy is implemented in [DTU Data](https://data.dtu.dk/DTU_Wind_Energy), ShareWind and in [CEDAR](cedar.metadatacenter.org/) through integration with [OntoPortal](https://bioportal.bioontology.org/ontologies/WETAXTOPICS/).

# Contribute

The taxonomy is intended to be used and further developed by the community. Therefore, we welcome collaborators willing to take part in the futher development of the taxonomy. If you are one of them please do so via GitHub by making pull requests and/or posting issues or requesting to become maintainer/developer of the taxonomy.

Specifically, to provide inputs to the taxonomy all you need to do is to update/modify (Excel sheet)[./taxonomy.xlsx], the rest is taken care of by the automatic workflow which on every update and corresponding push of the sheet will:

- Convert Excel file to RDF (turns Excel based taxonomy to machine-actionable form)
- Validate the converted taxonomy
- Deploy the taxonomy to OntoStack to be served at http://data.windenergy.dtu.dk/ontologies/view/

For the above workflow to function accordingly **DO NOT CHANGE THE FORM OF THE SHEET**, only update appropriate cells, or insert additional rows to define new terms in the taxonomy.
