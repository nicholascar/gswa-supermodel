# WA Boreholes Profile

<!--
<div style="text-align:right;">
    <div style="float:right; text-align:left; width: 30%; border:solid 2px #10797E; padding:10px; margin-left:5px; background-color: rgb(240, 240, 240);">
        <p>Machine-readable RDF:</p>
        <ul>
            <li><a href="https://raw.githubusercontent.com/nicholascar/gswa-supermodel/main/rdf/wa-borehole.ttl">Profile Definition</a></li>
            <li><a href="">Schema</a></li>
        </ul>
    </div>
</div>
-->

This profile contains a model of, and supporting schemas, vocabularies validators and example data for boreholes, also known as well bores.

The following figure shows some major physical elements of a borehole that this profile caters for, as well as alternative names for them, in _italics_.

<figure markdown>
  ![](../assets/boreholes-concepts.svg)
  <figcaption>Figure BC: Borehole Concepts. A Borehole (also known as a Well) consists of one or more Bores (Wellbores) into the earth. Geology of the earth may be characterised according to Borehole Intervals (Wellbore Intervals). The Borehole starts at a single origin point on the surface of the earth which may be on land or below the sea.</figcaption>
</figure>

## Resources

This Profile is made of many resources, all of which are contained in, or linked to from, this document. The resources and their roles are:

**Resource** | **Role**
--- | ---
Profile Definition | defines this set of resources - this table and text above
[Specification](#specification) | _[specification](https://www.w3.org/TR/dx-prof/#Role:specification)_<br />defines the profile elements in human-readable form
[Schema](#schema) | _[schema](https://www.w3.org/TR/dx-prof/#Role:schema)_<br />machine-readable version of the Specification's elements
[Validator](#validators) | _[validation](https://www.w3.org/TR/dx-prof/#Role:validation)_<br />machine-executable rules to test data for conformance to this Profile
[Compounded Validator](#validators) | _[validation](https://www.w3.org/TR/dx-prof/#Role:validation)_<br />this profile's validator & those of all dependencies in one
[Vocabularies](#vocabularies) | _[vocabulary](https://www.w3.org/TR/dx-prof/#Role:vocabulary)_<br />defines terms used in the profile specification
[Examples](#examples) | _[example](https://www.w3.org/TR/dx-prof/#Role:schema)_<br />valid and invalid data files
[Code Repository](#code-repository) | _[repository](https://www.w3.org/TR/dx-prof/#Role:schema)_<br />an online repository storing all of this Profile's resources

This is an interpretation of [GeoSciML](../background.md#geosciml)'s non-Semantic Web Boreholes model in Semantic Web form, with alignments to [GeoSPARQL](../background.md#geosparql) (for spatiality) and [SOSA](../background.md#sensor-observation-sample-and-actuator-ontology-sosa) (for sampling features & systems) realised through this being a profile of the [FSDF Backbone Model](https://linked.data.gov.au/def/fsdf-backbone), since that profiles GeoSPARQL and SOSA.

This profile's dependencies, as stated above, are shown graphically, in the figure below.

<figure markdown>
  ![](../assets/boreholes-hierarchy.svg)
  <figcaption>Figure BH: Profile hierarchy of the Boreholes Profile</figcaption>
</figure>

## Specification

### Model Overview

Figure BO below is an [OWL](../background.md#web-ontology-language-owl) diagram of the major components of this profile's model. Where they match, the names of the classes in this Figure link them to the elements in the Concepts, [Figure BC](boreholes-profile.md) above.

> The Key for the elements in this Figure is the [main key for this Supermodel](../supermodel.md#modelling-conventions).

<figure markdown>
  ![](../assets/boreholes-model.svg)  
  <figcaption>Figure BO: Overview of the model of this Borehole Profile. The Borehole class may be related to zero or more Bores which, in turn, may have zero or more Borehole Intervals. Borehole & Bores are geospatial Features and may have Geometries and Samples may be taken of Boreholes. Boreholes may be attributed to Agents (people and organisations) with the attribution qualified with Roles. A number of vocabulary-based classifiers are available for the Borehole, such as Borehole Purpose whose values are selected from controlled vocabularies supplied within this Profile.</figcaption>
</figure>

### Classes

**Property** | **Value**
--- | ---
IRI | https://linked.data.gov.au/def/xxx/Borehole
Name | Borehole
Description | _Coming..._

### Properties

## Schema

## Validators

## Vocabularies

## Examples

```turtle
:x
    a gswa:Borehole ;
    rdfs:label "Borehole X" ;
    geo:hasGeometry [
        geo:asWKT "POINT (123, -45)
    ] ;
    
```

# Code Repository
