# Country Music Hall of Fame Mapping

## About

This document describes the country music hall of fame mapping from QDC to MODS.

## Repository Structure

```
|-- cleaned_data
	|-- modsxml
    	|-- cmhf1.xml
        |-- cmhf2.xml
    |-- remediation_files
    	|-- countrymusic_refinetemplate.md
        |-- mods_collection.xml
        |-- split_collection.xsl
|-- original_data
	|-- countryqdc.xml
|-- REAME.md
```

## Goals

For CMHF, only grab records that have one of these three exact matches in dc:format (1325 total records):

1. 6.5 inch metal-based acetate disc (48 records)
2. 10 inch metal-based acetate disc (1172 records)
3. 8 inch metal-based acetate disc (105 records)

## Metadata Mapping

| QDC Field | MODS Field | MAP 4 Field | Note|
| -----| ------- | ------ | --- |
| dc:identifier | /identifier | sourceResource.identifier | |
| dc:title | /titleInfo/title | sourceResource.title | |
| dc:accessRights | /accessCondition | sourceResource.rights | |
| dc:rightsHolder | **NONE** | sourceResource.rightsHolder| Currently, we don't map this, although we could.|
| dc:format | /physicalDescription/form | sourceResource.format | |
| dc:tableOfContents | **NONE** | **NONE** |  |
| dc:description | /abstract | sourceResource.description | |
| dcterms:created | **NONE**  | ???? | |
| dc:subject | ```<subject><topic>/<name>/<titleInfo><title>/<genre>/<occupation>``` | | |
| dc:creator | ```<name><namePart>[value]</namePart><role> <roleTerm>Creator</roleTerm></role></name>``` | | |
| dc:date | originInfo/dateCreated | | From Gretchen's mapping notes: **originInfo/dateCreated** (use all instances. Some have qualifier indicating EDTF format and keyDate, others are qualified as "approximate"). Dates are in the format: **YYYY-MM-DD**. |
| dcterms:isPartOf | **NONE** | **NONE** | This should describe the collection it belongs to, but doesn't. |
| **NONE** | /recordInfo/recordContentSource | sourceResource.dataProvider | Use string: **Country Music Hall of Fame**|
| dc:identifier | ```<location><url usage="primary" access="object in context">``` | | if it starts with http|
| **NONE** | ```<location><url access="preview">``` | | take identifier, test if http, then use this pattern: |



## As QDC

**Note**: this includes records with dc:formats that we're not extracting.

| key                                                  | types                   | occurrences | percents           |
| ---------------------------------------------------- | ----------------------- | ----------- | ------------------ |
| _id                                                  | ObjectId                |        4879 | 100.00000000000000 |
| metadata                                             | Object                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc                         | Object                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.@xmlns:dc               | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.@xmlns:dcterms          | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.@xmlns:oai_qdc          | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.@xmlns:xsi              | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.@xsi:schemaLocation     | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.dc:identifier           | Array (4874),String (5) |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.dc:source               | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.dc:title                | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.dcterms:accessRights    | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.dcterms:rightsHolder    | String                  |        4879 | 100.00000000000000 |
| oai_provider                                         | String                  |        4879 | 100.00000000000000 |
| record_id                                            | String                  |        4879 | 100.00000000000000 |
| metadata.oai_qdc:qualifieddc.dc:format               | Array (4868),String (9) |        4877 |  99.95900799344128 |
| metadata.oai_qdc:qualifieddc.dcterms:tableOfContents | String (4871),Array (3) |        4874 |  99.89751998360320 |
| metadata.oai_qdc:qualifieddc.dc:description          | String                  |        4855 |  99.50809592129535 |
| metadata.oai_qdc:qualifieddc.dcterms:created         | String                  |        4840 |  99.20065587210495 |
| metadata.oai_qdc:qualifieddc.dc:subject              | String                  |        4486 |  91.94507071121132 |
| metadata.oai_qdc:qualifieddc.dc:creator              | String                  |        4138 |  84.81246156999386 |
| metadata.oai_qdc:qualifieddc.dc:date                 | String                  |        3496 |  71.65402746464440 |
| metadata.oai_qdc:qualifieddc.dcterms:isPartOf        | String                  |        3374 |  69.15351506456241 |

## As MODS

| key                                            | types                    | occurrences | percents            |
| ---------------------------------------------- | ------------------------ | ----------- | ------------------- |
| _id                                            | ObjectId                 |        1325 | 100.000000000000000 |
| metadata                                       | Object                   |        1325 | 100.000000000000000 |
| metadata.mods                                  | Object                   |        1325 | 100.000000000000000 |
| metadata.mods.@xmlns                           | String                   |        1325 | 100.000000000000000 |
| metadata.mods.@xmlns:xlink                     | String                   |        1325 | 100.000000000000000 |
| metadata.mods.@xmlns:xs                        | String                   |        1325 | 100.000000000000000 |
| metadata.mods.@xmlns:xsi                       | String                   |        1325 | 100.000000000000000 |
| metadata.mods.@xsi:schemaLocation              | String                   |        1325 | 100.000000000000000 |
| metadata.mods.accessCondition                  | String                   |        1325 | 100.000000000000000 |
| metadata.mods.identifier                       | Object                   |        1325 | 100.000000000000000 |
| metadata.mods.identifier.#text                 | String                   |        1325 | 100.000000000000000 |
| metadata.mods.identifier.@type                 | String                   |        1325 | 100.000000000000000 |
| metadata.mods.location                         | Array                    |        1325 | 100.000000000000000 |
| metadata.mods.location.XX.url                  | Object                   |        1325 | 100.000000000000000 |
| metadata.mods.location.XX.url.#text            | String                   |        1325 | 100.000000000000000 |
| metadata.mods.location.XX.url.@access          | String                   |        1325 | 100.000000000000000 |
| metadata.mods.location.XX.url.@usage           | String                   |        1325 | 100.000000000000000 |
| metadata.mods.physicalDescription              | Array                    |        1325 | 100.000000000000000 |
| metadata.mods.physicalDescription.XX.form      | String                   |        1325 | 100.000000000000000 |
| metadata.mods.recordInfo                       | Object                   |        1325 | 100.000000000000000 |
| metadata.mods.recordInfo.recordContentSource   | String                   |        1325 | 100.000000000000000 |
| metadata.mods.titleInfo                        | Object                   |        1325 | 100.000000000000000 |
| metadata.mods.titleInfo.title                  | String                   |        1325 | 100.000000000000000 |
| oai_provider                                   | String                   |        1325 | 100.000000000000000 |
| record_id                                      | String                   |        1325 | 100.000000000000000 |
| metadata.mods.abstract                         | String                   |        1316 |  99.320754716981128 |
| metadata.mods.name                             | Object (828),Array (234) |        1062 |  80.150943396226410 |
| metadata.mods.subject                          | Array (529),Object (483) |        1012 |  76.377358490566039 |
| metadata.mods.name.namePart                    | String                   |         828 |  62.490566037735846 |
| metadata.mods.name.role                        | Object                   |         828 |  62.490566037735846 |
| metadata.mods.name.role.roleTerm               | String                   |         828 |  62.490566037735846 |
| metadata.mods.subject.XX.topic                 | String                   |         529 |  39.924528301886795 |
| metadata.mods.originInfo                       | Object                   |         506 |  38.188679245283019 |
| metadata.mods.originInfo.dateCreated           | Object                   |         506 |  38.188679245283019 |
| metadata.mods.originInfo.dateCreated.#text     | String                   |         506 |  38.188679245283019 |
| metadata.mods.originInfo.dateCreated.@encoding | String                   |         506 |  38.188679245283019 |
| metadata.mods.originInfo.dateCreated.@keyDate  | String                   |         506 |  38.188679245283019 |
| metadata.mods.subject.topic                    | String                   |         483 |  36.452830188679243 |
| metadata.mods.name.XX.namePart                 | String (234),null (3)    |         234 |  17.660377358490567 |
| metadata.mods.name.XX.role                     | Object                   |         234 |  17.660377358490567 |
| metadata.mods.name.XX.role.roleTerm            | String                   |         234 | 