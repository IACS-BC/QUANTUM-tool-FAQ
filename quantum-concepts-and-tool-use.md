# QUANTUM concepts and tool use

#### Q1.- Our researchers are not familiar with PROV-O

A.- PROV-O is the "Provenance Ontology" proposed by the W3C consortium (https://www.w3.org/TR/prov-o/), and it is the standard provenance ontology chosen by Health DCAT-AP. Data provenance is a key attribute of the quality and utility of a dataset, as you should provide information about the source of your dataset, and the transformations applied to the data from the original source to your repository. Manual provenance management is not the best way to deal with this information, and it is optimal to use data management software that takes care of that, and in that case, you data management tool will be compliant to PROV-O or other provenance standard. If you do this management, or aim to do it, in a manual way, it will be a good practice to follow the PROV-O ontology and recommendations.

#### Q2.- An example of HealthDCAT-AP

A.-

```turtle
<https://registries.example.gov/national-cancer-registry> a dcat:Dataset ;
    dct:title ""National Cancer Registry of Spain""@es ;
    dct:description ""A comprehensive registry of all cancer diagnoses reported in Spain, including demographic, clinical, and treatment information. Data is updated annually.""@es ;
    dcat:keyword ""cáncer""@es, ""epidemiología""@es, ""salud pública""@es ;
    dcat:theme <http://snomed.info/id/363358000> ; # SNOMED CT concept for ""Malignant neoplastic disease""
    dct:publisher [
        a foaf:Agent ;
        foaf:name ""Ministry of Health of Spain""
    ] ;
    dcat:contactPoint [
        a vcard:Organization ;
        vcard:fn ""Registry Information Office"" ;
        vcard:hasEmail <mailto:info-registry@health.example.gov>
    ] ;
    dcat:distribution [
        a dcat:Distribution ;
        dct:title ""Web Portal for Data Queries"" ;
        dcat:accessURL <https://registries.example.gov/national-cancer-registry/query-tool> ;
        dct:format <http://publications.europa.eu/resource/authority/file-type/HTML> ;
        dcat:mediaType ""text/html"" ;
        dct:description ""Access is provided through an online query tool for aggregated data. Access to microdata requires a formal application.""@es
    ] .

```

### Q3.- What does "Compliance" refer to in the context of data, and what kind of documentation is required to demonstrate it?

A.- Compliance refers to the degree to which data and its handling processes adhere to established ethical standards, conventions, protocols, or regulations. Documenting this is crucial to ensure transparency and accountability.

It is important to understand that the need for ethical compliance documentation is not exclusive to clinical trials. It also applies to observational studies and any other research that involves the use of secondary data.

You should include in this attribute, for example, documentation about ethical committee's approval (if needed), Data Protection Impact Assessments, DPOs reportings, security or data protection certifications, etc.



### Q4.- How should 'time to access' be calculated for a dataset with multiple components that have different access times (e.g., a mix of instantly available open data and restricted data that requires approval)?

For a complex dataset with components that have different access times, the reported "time to access" should always be the longest time required. In other words, the metric must represent the total time until all requested components of the dataset are fully available to the user.



### Q5.- Does the time to access truly reflect data quality?

While not an intrinsic quality dimension of the data itself, access time can be a critical factor in the decision to use a dataset. This metric can be measured by the HDAB, but its scope must be clearly defined.

The measurement should only cover the period from the data holder's reception of the application to the actual data access or release. It must not include the initial application processing time handled by the HDAB.



### Q6.- How long does it take to complete the survey?

It depends on your level of maturity and your knowledge of your dataset and metadata. If you've already assessed the quality of your datasets and have the documentation, we estimate the survey will take no more than an hour. Based on feedback from other users of the tool, we estimate an investment of one to four hours, depending on your maturity and experience managing datasets. If you assess more than one dataset, subsequent datasets will take much less time.



### Q7.- What is W3C?

The W3C, or World Wide Web Consortium, is an international organization that develops open standards and protocols for the web to ensure its long-term growth. Its mission is to make the web accessible, secure, and usable for everyone.

### &#x20;Q8.- What is the difference between a catalogue and a dataset?

A Catalogue can have two definitions, comprising: 1. data or 2. metadata.

1. A data Catalogue (or Catalog) is a curated collection of datasets and data services that are managed and published by an organisation or entity.
2. A data catalogue is a curated collection of metadata about datasets that are managed and published by an organisation or entity.

A Dataset is a collection of data, published or curated by a single source, and available for access or download in one or more formats.

Within the context of the EHDS (European Health Data Space) Regulation proposal \[EUR-Lex 52022PC0197 (Art.44)], access to such datasets must adhere to principles of data minimisation and purpose limitation. This ensures that only the data relevant and necessary for specific processing purposes is provided. This data can be in either anonymised or pseudonymised format depending on the feasibility of achieving the processing objectives.



### Q9.- What is an RDF?

RDF (Resource Description Framework) is a standard model for describing and structuring data on the web. It represents information as triples, where each triple consists of:

* **Subject** (the entity being described)
* **Predicate** (the relationship or property of the subject)
* **Object** (the value or another entity related to the subject)

This structure allows RDF to create interconnected, machine-readable data, enabling data interoperability and linking across different sources.

RDF data can be serialized in various formats, including Turtle, RDF/XML, and JSON-LD, and is commonly used in the Semantic Web, linked data, and metadata management.

RDF is widely used in data catalogs (DCAT), data quality assessment (DQV), and knowledge graphs, ensuring structured and meaningful data representation across platforms.



### Q10.- Who should be fulfilling the survey?

Regarding the institution, it must be the data owner. If we ask about the person or profile who should be in charge of this task, it is up to each institution. It could be a Data Chief Officer, a Data Quality Manager, or a Data Manager. It is important that the person completing the form be someone with in-depth knowledge of data and its uses.<br>

<br>
