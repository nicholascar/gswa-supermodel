# WA Boreholes Profile

<div style="text-align:right; height: 100px;">
    <div style="float:right; text-align:left; width: 250px; border:solid 2px #10797E;">
        <p>Machine-readable version:</p>
        <ul><li><a href="static/rdf/wa-borehole.ttl">RDF Turtle format</a></li></ul>
    </div>
</div>

This is an interpretation of [GeoSciML](background.md#geosciml)'s non-Semantic Web Boreholes model in Semantic Web form, with alignments to [GeoSPARQL](background.md#geosparql) (for spatiality) and [SOSA](background.md#sensor-observation-sample-and-actuator-ontology-sosa) (for sampling features & systems) realised through this being a profile of the [FSDF Backbone Model](https://linked.data.gov.au/def/fsdf-backbone), since that profiles GeoSPARQL and SOSA.

This profile's dependencies, as stated above, are shown graphically, in the figure below.

<figure markdown>
  ![](../assets/boreholes-hierarchy.svg)
  <figcaption>Figure BH: Profile hierarchy of the Boreholes Profile</figcaption>
</figure>

Given the 

In essence, a _Borehole_ is both a kind of spatial feature - something that is somewhere - and also a thing which takes samples of something else to characterise it - samples of a portion of the earth's crust. 

The figure below is an [OWL](background.md#web-ontology-language-owl) diagram of the major components within this profile, including the [Background Model](background.md) elements which they profile.

<figure markdown>
  ![](../assets/boreholes-profile-overview.svg)  
  <figcaption>Figure BO: Overview diagram of this Borehole Profile</figcaption>
</figure>

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
