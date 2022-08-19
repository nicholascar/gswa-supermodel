# Boreholes Profile

This is a profile of [GeoSPARQL](background.md#geosparql) (for spatiality) and [SOSA](background.md#sensor-observation-sample-and-actuator-ontology-sosa) (for sampling features & systems). In essence, a _Borehole_ is both a kind of spatial feature - something that is somewhere - and also a thing which takes samples of something else to characterise it - samples of a portion of the earth's crust. 

The figure below is an [OWL](background.md#web-ontology-language-owl) diagram of the major components within this profile, including the [Background Model](background.md) elements which they profile.

![](../assets/boreholes-profile-overview.svg)  
<div style="text-align:center;">
<strong>Figure:</strong> Overview diagram of this Borehole Profile
</div>

## Classes & Properties

### Classes

**Property** | **Value**
--- | ---
IRI | https://linked.data.gov.au/def/xxx/Borehole
Name | Borehole
Description | _Coming..._

### Properties


## Vocabularies

## Validators

## Extended Example

```turtle
:x
    a gswa:Borehole ;
    rdfs:label "Borehole X" ;
    geo:hasGeometry [
        geo:asWKT "POINT (123, -45)
    ] ;
    
```
