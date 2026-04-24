# Organizational Maturity Label

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

