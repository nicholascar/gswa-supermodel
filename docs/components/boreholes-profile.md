# Boreholes Profile

This profile contains a model of, and supporting schemas, vocabularies validators and example data for **boreholes**, also known as well bores.

The Semantic Web model component of this Profile, it's schema, is published online at:

* **<https://linked.data.gov.au/def/borehole>**

## Overview

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
[Schema](#schema) | _[schema](https://www.w3.org/TR/dx-prof/#Role:schema)_<br />machine-readable version of the Specification's elements<br /><br />This is the Semantic Web model within this profile, online at <https://linked.data.gov.au/def/borehole>
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

> The Key for the elements in this Figure is the [figure key for this Supermodel](../supermodel.md#modelling-conventions).

<figure markdown>
  ![](../assets/boreholes-model.svg)  
  <figcaption>Figure BO: Overview of the model of this Borehole Profile. The Borehole class may be related to zero or more Bores which, in turn, may have zero or more Borehole Intervals. Borehole & Bores are geospatial Features and may have Geometries and Samples may be taken of Boreholes. Boreholes may be attributed to Agents (people and organisations) with the attribution qualified with Roles. A number of vocabulary-based classifiers are available for the Borehole, such as Borehole Purpose whose values are selected from controlled vocabularies supplied within this Profile.</figcaption>
</figure>

### Namespaces

The following prefixed namespaces are used in the code examples following:

**Prefix** | **Namespace** | **Description**
--- | --- | ---
`ex:` | `http://example.com/` | Generic, non-resolvable, examples
`bh:` | `http://linked.data.gov.au/def/borehole/` | This profile's schema/model
`bsp:` | `http://linked.data.gov.au/def/borehole-start-point/` | Borehole Start Point vocabulary, managed by the Geological Survey of Queensland
`dcat:` | `http://www.w3.org/ns/dcat#` | Data Catalogue vocabulary: cataloguing international standard
`geo:` | `http://www.opengis.net/ont/geosparql#` | GeoSPARQL: Semantic Web spatial international standard
`prov:` | `http://www.w3.org/ns/prov#` | Provenance Ontology: provenance data structures international standard


### Classes

#### Borehole

**Property** | **Value**
--- | ---
IRI | [`bh:Borehole`](https://linked.data.gov.au/def/borehole/Borehole)
[Name](https://schema.org/name "sdo:name") | Borehole
[Description](https://schema.org/description "sdo:description") | A borehole is a narrow shaft bored in the ground. A borehole may be constructed for many different purposes, including the extraction of water, other liquids (such as petroleum) or gases (such as natural gas), as part of a geotechnical investigation, environmental site assessment, mineral exploration, temperature measurement, as a pilot hole for installing piers or underground utilities, for geothermal installations, or for underground storage of unwanted substances, e.g. in carbon capture and storage.

[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example")

```
ex:bh-01
    a bh:Borehole ;
    bh:hasOriginPosition [
        geo:asWKT "POINT (153.083340 -27.325458)"^^geo:wktLiteral ;
    ] ;
    bh:hasSurfaceCircumstance bsp:natural-ground-surface ;
    prov:wasAttributedTo [
        prov:agent <https://orcid.org/0000-0002-8742-7730> ;
        dcat:hadRole ex:driller ;
    ] ;
.
```
This example shows a borehole, `ex:bh-01`, with an origin position at longitude 153.083340 E & latitude 27.325458 S, a surface circumstance taken from a Geological Survey of Queensland vocabulary ("natural ground surface") and there's an attribution of the borehole to an Agent: Nicholas Car, identified by an IRI, with the role of driller.

#### Bore

**Property** | **Value**
--- | ---
IRI | [`bh:Bore`](https://linked.data.gov.au/def/borehole/Bore)
[Name](https://schema.org/name "sdo:name") | Bore
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

#### Borehole Interval

**Property** | **Value**
--- | ---
IRI | [`bh:BoreholeInterval`](https://linked.data.gov.au/def/borehole/BoreholeInterval)
[Name](https://schema.org/name "sdo:name") | Borehole Interval
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

### Properties

#### has origin position

**Property** | **Value**
--- | ---
IRI | [`bh:hasOriginPosition`](https://linked.data.gov.au/def/borehole/hasOriginPosition)
[Name](https://schema.org/name "sdo:name") | has origin position
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

#### has log element

**Property** | **Value**
--- | ---
IRI | [`bh:hasLogElement`](https://linked.data.gov.au/def/borehole/hasLogElement)
[Name](https://schema.org/name "sdo:name") | has log element
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

#### has purpose

**Property** | **Value**
--- | ---
IRI | [`bh:hasPurpose`](https://linked.data.gov.au/def/borehole/hasPurpose)
[Name](https://schema.org/name "sdo:name") | has purpose
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

#### has inclination

**Property** | **Value**
--- | ---
IRI | [`bh:hasInclination`](https://linked.data.gov.au/def/borehole/hasInclination)
[Name](https://schema.org/name "sdo:name") | has inclination
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

#### has surface circumstances

**Property** | **Value**
--- | ---
IRI | [`bh:hasSurfaceCircumstances`](https://linked.data.gov.au/def/borehole/hasSurfaceCircumstances)
[Name](https://schema.org/name "sdo:name") | has surface circumstances
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

#### has status

**Property** | **Value**
--- | ---
IRI | [`bh:hasStatus`](https://linked.data.gov.au/def/borehole/hasStatus)
[Name](https://schema.org/name "sdo:name") | has status
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

#### had drilling method

**Property** | **Value**
--- | ---
IRI | [`bh:hadDrillingMethod`](https://linked.data.gov.au/def/borehole/hadDrillingMethod)
[Name](https://schema.org/name "sdo:name") | had drilling method
[Description](https://schema.org/description "sdo:description") | _Coming..._
[Example](https://www.w3.org/TR/skos-reference/#notes "skos:example") | 

## Schema

## Validators

## Vocabularies

## Examples

This section presents complete (valid, according to this profile) RDF data examples. The first is compounded from the snippet examples from the [Specification Section](#specification) above. 

#### E.g. 01 [:octicons-link-external-16:](https://github.com/nicholascar/gswa-supermodel/blob/main/rdf/borehole/examples/eg-01.ttl)

```turtle
ex:bh-01
    a bh:Borehole ;
    prov:wasAttributedTo [
        a prov:Attribution ;
        dcat:hadRole ex:driller ;
        prov:agent <https://orcid.org/0000-0002-8742-7730>
    ] ;
    bh:hasOriginPosition [
        a geo:Geometry ;
        geo:asWKT "POINT (153.083340 -27.325458)"^^geo:wktLiteral
    ] ;
    bh:hasSurfaceCircumstance bsp:natural-ground-surface ;
.

<https://orcid.org/0000-0002-8742-7730>
    a sdo:Person ;
    sdo:email "nick@kurrawong.net"^^xsd:anyURI ;
    sdo:name "Nicholas J. Car"@en ;
.
```

## Code Repository

While a copy of all Borehole Profile resources are contained within the repository for the GSWA Supermodel, the home location of this profile is:

* <https://github.com/geological-survey-of-queensland/gsq-borehole-profile/>
