

# INTERACT Data guidelines v 0.01

#### Minimum necessary fields for Dataset ([science-on-schema.org](https://github.com/ESIPFed/science-on-schema.org/blob/master/guides/Dataset.md), [DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Class:Dataset))



## name

#### Type: [Text](https://schema.org/Text)
#### Field name:
[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_title):  dct:title 

[Science-on-schema.org](https://github.com/ESIPFed/science-on-schema.org/blob/master/guides/Dataset.md#common-properties): name

#### Description:

A descriptive name of a dataset.

#### Guidelines:

-   The title must be an alphanumeric string between 50 and 500 characters long.

#### Example (in JSON-LD format):
```json
 "name": "Removal of organic carbon by natural bacterioplankton communities as a function of pCO2 from laboratory experiments between 2012 and 2016"
```
#### Example (in DCAT-AP format):
```xml
<dct:title xml:lang="en">Nobel Media Dataset catalog</dct:title>
```

## description

#### Type:   [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_description):  dct:description

[Science-on-schema.org](https://github.com/ESIPFed/science-on-schema.org/blob/master/guides/Dataset.md#common-properties): description

#### Description:

A short summary describing a dataset.

#### Guidelines:

-   The summary must be an alphanumeric string between 50 and 5000 characters long.

-   When using the JSON-LD format, denote new lines with \n (two characters: backslash and lowercase letter "n").

#### Example (in JSON-LD format):
```json
 "description": "This dataset includes results of laboratory experiments which measured dissolved organic carbon (DOC) usage by natural bacteria in seawater at different pCO2 levels. Included in this dataset are; bacterial abundance, total organic carbon (TOC), what DOC was added to the experiment, target pCO2 level. "

```
#### Example (in DCAT-AP format):
```xml
<dct:description xml:lang="en">This dataset includes results of laboratory experiments which measured dissolved organic carbon (DOC) usage by natural bacteria in seawater at different pCO2 levels. Included in this dataset are; bacterial abundance, total organic carbon (TOC), what DOC was added to the experiment, target pCO2 level.</dct:description>\
```

## keywords

#### Type: [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_keyword):  dct:keywords

[Science-on-schema.org](https://schema.org/keywords): keywords

#### Description:

Keywords summarizing the dataset.

#### Guidelines:

##### DCAT-AP

Use a keyword tag for each keyword.The value of each tag must be an alphanumeric string.

##### JSON-LD

Value must be a valid list of alphanumeric strings separated by a comma.

#### Examples (in JSON-LD format):
```json
 "keywords": ["ocean acidification", "Dissolved Organic Carbon", "bacterioplankton respiration", "pCO2", "carbon dioxide", "oceans"]
```
#### Examples (in DCAT-AP format):
```xml
<dcat:keyword>oceans</dcat:keyword>

<dcat:keyword>carbon dioxide</dcat:keyword>

<dcat:keyword>pCO2</dcat:keyword>
 ```

## url 


#### Type: [URL](https://schema.org/URL)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat/#Property:dataset_landingpage):  dct:landingpage

[Science-on-schema.org](https://schema.org/url): url

#### Description:

Location of a page describing the dataset.

#### Guidelines:

Value must be a valid URL.

#### Examples (in JSON-LD format):
```json
 "url": "https://www.sample-data-repository.org/dataset/472032",
```

#### Examples (in DCAT-AP format):
```xml

<dcat:landingPage>

<foaf:Document rdf:about="http://geonetwork.bmdc.be/geonetwork/srv/eng/catalog.search#/metadata/ee056fd6-995e-40a7-8ebf-b145ea0a30e0"/>

</dcat:landingPage>
```


## citation


#### Type:  [Text](https://schema.org/Text) or [CreativeWork](https://schema.org/CreativeWork)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_identifier):  dct:identifier

[Science-on-schema.org](https://schema.org/citation): citation

#### Description:

Identifies academic articles that are recommended by the data provider be cited in addition to the dataset itself. Provide the citation for the dataset itself with other properties, such as name, identifier, creator, and publisher properties. For example, this property can uniquely identify a related academic publication such as a data descriptor, data paper, or an article for which this dataset is supplementary material for. 

#### Guidelines:

-   When populating the citation property with a citation snippet, provide the article identifier (such as a DOI) whenever possible.\
    Recommended: "Doe J (2014) Influence of X. Biomics 1(1). https://doi.org/10.1111/111"\
    Not recommended: "Doe J (2014) Influence of X. Biomics 1(1)."

#### Examples (in JSON-LD format):
```json

"citation": "https://doi.org/10.1111/111"

"citation": "https://identifiers.org/pubmed:11111111"

"citation": "https://identifiers.org/arxiv:0111.1111v1"

"citation":

 "Doe J (2014) Influence of X ... https://doi.org/10.1111/111"
```
#### Examples (in DCAT-AP format):
```xml

 <dct:identifier>

https://doi.org/10.25919/5b4d2b83cbf2d

</dcat:identifier>
```
 

## creator



#### Type: [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_creator):  dct:creator

[Science-on-schema.org](https://schema.org/creator): creator

#### Description:

The author of the content

#### Examples (in JSON-LD format):
```json
 "creator": [

    {

      "@id": "https://www.sample-data-repository.org/person-role/472036",

      "@type": "Role",

      "roleName": "Principal Investigator",

      "creator": {

        "@id": "https://www.sample-data-repository.org/person/51317",

        "@type": "Person",

        "name": "Dr Uta Passow",

        "givenName": "Uta",

        "familyName": "Passow",

        "url": "https://www.sample-data-repository.org/person/51317"

      }

    }
```
#### Examples (in DCAT-AP format):


## topicCategory

 
#### Type: [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_theme):  dct:theme

[Science-on-schema.org](https://schema.org/about): about

#### Description:

The subject matter of the content. 

#### Guidelines:

Use INTERACT's list of approved topics. 

(to be defined)

#### Examples (in JSON-LD format):
```json
"about":"environment"
```
#### Examples (in DCAT-AP format):
```xml
<dct:theme>environment</dct:theme>
```

## temporalCoverage



#### type: [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:dataset_temporal):  dct:temporal

[Science-on-schema.org](http://schema.org/temporalCoverage): temporalCoverage

#### Description:

The temporal period that the dataset covers.

#### Guidelines:

Use the ISO 8601 standard to describe time intervals and time points. You can describe dates differently depending upon the dataset interval. Indicate open-ended intervals with two decimal points (..).

#### Examples (in JSON-LD format):

#####   Single date
```json
"temporalCoverage" : "2008"
```

##### Time period
```json
"temporalCoverage" : "1950-01-01/2013-12-18"
```

#####   Open-ended time period
```json
"temporalCoverage" : "2013-12-19/.."
```
---
#### Examples (in DCAT-AP format):
```xml
<dct:temporal>

<dct:PeriodOfTime>

    <schema:startDate>2009-07-28</schema:startDate>
    <schema:endDate>2009-11-20</schema:endDate>

</dct:PeriodOfTime>

</dct:temporal>
 ```


## spatialCoverage


#### Type: [Text](https://schema.org/Text), [Place](https://schema.org/Place)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:dataset_spatial):  dct:spatial

[Science-on-schema.org](https://github.com/ESIPFed/science-on-schema.org/blob/master/guides/Dataset.md#spatial-coverage): spatialCoverage

#### Description:

The geographical area or point covered by the dataset.

#### Guidelines:

You can provide a single point that describes the spatial aspect of the dataset. Only include this property if the dataset has a spatial dimension. For example, a single point where all the measurements were collected, or the coordinates of a bounding box for an area.

#### Examples (in JSON-LD format):

##### Points
```json
"spatialCoverage:" {

  "@type": "Place",

  "geo": {

    "@type": "GeoCoordinates",

    "latitude": 39.3280,

    "longitude": 120.1633

  }

}
```
##### Shapes

Use [GeoShape](https://schema.org/GeoShape) to describe areas of different shapes. For example, to specify a bounding box.

```json
 "spatialCoverage:" {

  "@type": "Place",

  "geo": {

    "@type": "GeoShape",

    "box": "39.3280 120.1633 40.445 123.7878"

  }

}
```
Points inside box, circle, line, or  polygon  properties must be expressed as a space separated pair of two values corresponding to latitude and longitude (in that order).

##### Named locations

```json
"spatialCoverage:"  "Tahoe City, CA"
```
---
#### Examples (in DCAT-AP format):
```xml
<dct:spatial  rdf:resource="http://geonames/Newark">

    <dct:Location>

        <locn:geometry  rdf:datatype="https://www.iana.org/assignments/media-types/application/vnd.geo+json">

            {"type": "Polygon", "coordinates": [[[175.0, 17.5], [-65.5, 17.5], [-65.5, 72.0], [175.0, 72.0], [175.0, 17.5]]]}

        </locn:geometry>

        <locn:geometry  rdf:datatype="http://www.opengis.net/ont/geosparql#wktLiteral">

            POLYGON ((175.0000 17.5000, -65.5000 17.5000, -65.5000 72.0000, 175.0000 72.0000, 175.0000 17.5000))

        </locn:geometry>

    </dct:Location>

</dct:spatial>
```

## datePublished

#### Type: [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_release_date):  dct:issued

[Science-on-schema.org](https://schema.org/datePublished): datePublished

#### Description:

Date of formal publication of the item.

#### Guidelines:

Use ISO 8601 Date and Time compliant string

#### Examples (in JSON-LD format):
```json
"datePublished": "2005-05-22"
```
#### Examples (in DCAT-AP format):
```xml
<dct:issued rdf:datatype="&xsd;date">2012-01-15</dct:issued>
```
## dateModified



#### Type: [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_update_date):  dct:modified

[Science-on-schema.org](https://schema.org/dateModified): dateModified

#### Description:

Most recent date on which the item was changed, updated or modified

#### Guidelines:

Use ISO 8601 Date and Time compliant string

#### Examples (in JSON-LD format):
```json
"datePublished": "2015-05-22"
```
#### Examples (in DCAT-AP format):
```xml
<dct:modified rdf:datatype="&xsd;date">2015-05-25</dct:modified>\
 ```


## publisher

#### Type: [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_publisher):  dct:publisher

[Science-on-schema.org](https://schema.org/publisher): publisher

#### Description:

The entity responsible for making the item available.

#### Examples (in JSON-LD format):

#### Examples (in DCAT-AP format):
```xml
<dct:publisher rdf:resource="http://dati.gov.it/resource/Amministrazione/agid"/>\
 ```


## provider



#### Type: [Text](https://schema.org/Text)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:relationship_hadRole):  dcat:hadRole

[Science-on-schema.org](https://schema.org/provider): provider

#### Description:

The id of the entity that produced the metadata.

#### Guidelines:

Use INTERACT's list of approved identifiers for stations and partners. 

#### Examples (in JSON-LD format):

#### Examples (in DCAT-AP format):

## license

 

#### Type: [URL](https://schema.org/URL)
#### Field name:

[DCAT-AP](https://www.w3.org/TR/vocab-dcat-2/#Property:resource_license):  dct:license

[Science-on-schema.org](https://schema.org/license): license

#### Description:

A license document that applies to this content, typically indicated by URL.

#### Guidelines:

##### DCAT-AP

Use a license tag for each license.The value of each tag must be a valid URL.

##### JSON-LD

Value must be a list of valid URLs separated by a comma.

#### Examples (in JSON-LD format):
```json
 "license": [ "http://spdx.org/licenses/CC0-1.0", "https://creativecommons.org/publicdomain/zero/1.0"]
```
#### Examples (in DCAT-AP format):
```xml
<dct:license>

<dct:LicenseDocument rdf:about="http://creativecommons.org/publicdomain/zero/1.0/"/>

</dct:license>
```
 

## variableMeasured(to be discussed)

#### Type: [Text](https://schema.org/Text)
#### Field name:

DCAT-AP:  to be discussed

[Science-on-schema.org](https://schema.org/variableMeasured): variableMeasured

#### Description:

The variableMeasured property can indicate (repeated as necessary) the variables that are measured in some dataset, either described as text or as pairs of identifier and description using PropertyValue

#### Guidelines:
To be discussed
#### Examples (in JSON-LD format):
```json
"variableMeasured": [

  {"@type": "PropertyValue",

    "name": "Average air humidity",

    "description": "Average data recorded every minute for the previous period. The average is calculated by adding the measured values and then dividing the sum by the number of observations.",

    "unitText": "Percentage",

    "url": "http://www.cen.ulaval.ca/nordicanad/infounitedonnees.aspx?id=591304"

      }
```
#### Examples (in DCAT-AP format):

# Relevant resources:

1.  [DCAT-AP to schema.org](https://ec-jrc.github.io/dcat-ap-to-schema-org/)

2.  [Dublin Core Terminology](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)

3.  [DCAT Vocab](https://www.w3.org/TR/vocab-dcat-2/)

4.  [Google data guidelines](https://developers.google.com/search/docs/data-types/dataset)

5.  [Science-on-schema.org guide](https://github.com/ESIPFed/science-on-schema.org/blob/master/guides/)