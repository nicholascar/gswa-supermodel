# Backbone Model

## Intro

The _Backbone Model_ of this Supermodel is the core model that all _Component Model_ instances must conform to. This means that all data in all _Component Model_ instances must pass the _Backbone Model_ validator.

This model is actually a _profile_ of some _Background Models_, that is, it doesn't introduce much novel modelling but instead just selects elements from existing models and mandates particular patterns of use, such as requiring certain properties to be present. 

For example, this Model profiles [GeoSPARQL](background.md#geosparql), a well-known model used to model spatial objects, and uses GeoSPARQL elements to represent geospatial features and their geometries with GeoSPARQL's `Feature` and `Geometry` classes respectively. This means that any element within a _Component Model_ wishing to express spatiality, which will be a `Feature` of some sort such as a Well, must do so with GeoSPARQL's `hasGeometry` that relates a `Feature` to a `Geometry`.

## Profile

This model is formally defined as a profile of a number of standards in the profile definition:

* [Backbone Model Profile Declaration](https://github.com/nicholascar/gswa-supermodel/blob/main/rdf/backbone/profile.ttl)

This can be summarised like this: 

1. The _Backbone Model_ is a profile of [SOSA](background.md#sosa), [GeoSPARQL](background.md#geosparql), [AnzGeoDCAT](background.md#anzgeodcat) & [VocPub](background.md#vocpub) and, through them, [DCAT](background.md#dcat), [SKOS](background.md#skos). All of these are, in turn, profiles of [OWL](background.md#owl)
    1. see the figure below
2. It contains multiple profile resources:
    1. see the table below

This model's profile hierarchy is as follows:

<figure markdown>
  ![](assets/backbone-profiles.svg)  
  <figcaption>Figure BP: The Standards profiles by this Backbone Model.</figcaption>
</figure>

The profile resources and their roles are as follows:

**Resource** | **Role**
--- | ---
[Profile Declaration](https://github.com/nicholascar/gswa-supermodel/blob/main/rdf/backbone/profile.ttl) | profile definition
[Validator](https://github.com/nicholascar/gswa-supermodel/blob/main/rdf/backbone/validator.ttl) | [Validation](https://www.w3.org/TR/dx-prof/#Role:validation)
[Compounded Validator](https://github.com/nicholascar/gswa-supermodel/blob/main/rdf/backbone/validator-compounded.ttl) | [Validation](https://www.w3.org/TR/dx-prof/#Role:validation)
this documentation | [Specification](https://www.w3.org/TR/dx-prof/#Role:guidance) & [Guidance](https://www.w3.org/TR/dx-prof/#Role:guidance)


## Validator

* [Backbone Model validator](https://github.com/nicholascar/gswa-supermodel/blob/main/rdf/backbone/validator.ttl)

This validator only tests for specific rules encoded within this _Backbone Model_. 

To test data for full conformance to this _Backbone Model_ and all the things that this _Backbone Model_ profile, such as GeoSPARQL, VocPub etc., use the compounded validator:

* [Backbone Model compounded validator](https://github.com/nicholascar/gswa-supermodel/blob/main/rdf/backbone/validator-compounded.ttl)

This validator contains the Backbone Model validator and all dependent validators too.

## Requirements

This _Backbone Model_ ensures that the following requirements of data are met:

**ID** | **Title** | **Description**
--- | --- | --- 
R01 | Individually managed collection. of data must be modelled as [dcat:Dataset](https://www.w3.org/TR/vocab-dcat/#Class:Dataset) instances | Datasets are defined, described and registered in a catalogue
R02 | Datasets must have basic metadata | Datasets, modelled as [dcat:Dataset](https://www.w3.org/TR/vocab-dcat/#Class:Dataset) instances, must have the following properties recorded: [dcterms:title](https://www.w3.org/TR/vocab-dcat/#Property:resource_title), [dcterms:description](https://www.w3.org/TR/vocab-dcat/#Property:resource_description), [dcterms:created](http://purl.org/dc/terms/created) , [dcterms:modified](http://purl.org/dc/terms/modified), [dcat:contactPoint](https://www.w3.org/TR/vocab-dcat/#Property:resource_contact_point), [dcterms:publisher](https://www.w3.org/TR/vocab-dcat/#Property:resource_publisher) (this will usually be GSWA) 
R03 | |
... | | 
RXX | Geospatial objects must be modelled as [geo:Feature](https://opengeospatial.github.io/ogc-geosparql/geosparql11/spec.html#_class_geofeature) instances | Features have spatial projections as Geometries and may have spatial relations to other Features as well as non-spatial relations to other class instances