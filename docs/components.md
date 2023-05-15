# Component Models

This section lists the various Component Models within this Supermodel.

All data created according to any of the Component Models, to be used in this Supermodel's context, _MUST_ also conform to this Supermodel's [Backbone Model](backbone.md). 

Note that useful data may be created that is valid according to individual Component Models and not this Supermodels' Backbone Model for use outside this Supermodel's context.  

## Profiles

Many of the Component Models here are defined as a _profile_, by which we mean that it is a model that draws from other Standard's models and constrains and extends their elements, rather than creating its own elements.

Profiles are used to specialise general-purpose models while remaining conformant with them.
 
Formally, any data created according to a _profile_ _MUST_ conform to all the models it profiles, as per the [Profiles Vocabulary](background.md#profiles-vocabulary-prof) rules.

Profiles may profile multiple Standards, bringing together all the parts needed for a particular task

## List of Component Models

Several of the Component Models within this Supermodel are full defined here. Others are defined elsewhere and just referred to from here. The table below lists the current Component Models.

**Model** | **Domain(s)** | **Persistent Identifier** | **Notes**
--- | --- | --- | --- 
[Borehole Profile](components/boreholes.md) | boreholes | `https://linked.data.gov.au/def/borehole` |
[Samples Profile](components/samples.md) | samples, sampling | `https://linked.data.gov.au/def/xxx` | Coming...
[Geo Features Profile](components/geo-features.md) | geospatial spatial features | `https://linked.data.gov.au/def/xxx` | Coming...
[Sites & Admin Features Profile](components/sites-admin.md) | man-made & administrative spatial features | `https://linked.data.gov.au/def/xxx` | Coming...
