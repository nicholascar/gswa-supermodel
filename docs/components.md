# Component Models

This section lists the various Component Models within this Supermodel.

Several of the Component Models within this Supermodel are full defined here. Others are defined elsewhere and just referred to from here. The table below lists the current major Datasets in the FSDF Data Platform and their Component Models or use of the Backbone Model.

**Model** | **Domain(s)** | **Persistent Identifier** | **Notes**
--- | --- | --- | --- 
Borehole Profile | boreholes | `https://linked.data.gov.au/def/xxx` | Coming...
Samples Profile | samples, sampling | `https://linked.data.gov.au/def/xxx` | Coming...
Geo Features Profile | geospatial spatial features | `https://linked.data.gov.au/def/xxx` | Coming...
Admin Features Profile | administrative spatial features | `https://linked.data.gov.au/def/xxx` | Coming...

## Boreholes Profile

### Overview

This is a profile of [GeoSPARQL](background.md#geosparql) (for spatiality) and [SOSA](background.md#sensor-observation-sample-and-actuator-ontology-sosa) (for sampling features & systems). In essence, a _Borehole_ is both a kind of spatial feature - something that is somewhere - and also a thing which takes samples of something else to characterise it: samples of a portion of the earth's crust and potentially orebodies. 

> By _profile_ we mean that this model draws from other standards and mostly constrains and extends their elements, rather than creating its own.
> 
> Formally, any data created according to this _profile_ will conform to all the models it profiles, as per the [Profiles Vocabulary](background.md#profiles-vocabulary-prof) rules.

The figure below is an [OWL](background.md#web-ontology-language-owl) diagram of the major components within this profile, including the [Background Model](background.md) elements which they profile.


![](assets/boreholes-profile-overview.svg)  
<div style="text-align:center;">
<strong>Figure:</strong> Overview diagram of this Borehole Profile
</div>

### Classes & Properties

#### Classes

**Property** | **Value**
--- | ---
IRI | https://linked.data.gov.au/def/xxx/Borehole
Name | Borehole
Description | _Coming..._

#### Properties


### Vocabularies

### Validators

### Extended Example

```turtle
:x
    a gswa:Borehole ;
    rdfs:label "Borehole X" ;
    geo:hasGeometry [
        geo:asWKT "POINT (123, -45)
    ] ;
    
```

## Samples Profile

## Geo Features Profile

## Admin Features Profile