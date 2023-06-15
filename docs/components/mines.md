## Overview

<a href="../../assets/mines-Overview.svg">
<figure id="figure-bh" markdown style="width:100%">
  ![](../assets/mines-Overview.svg)
  <figcaption>Figure MO: Overview of this Mines Model</figcaption>
</figure>
</a>

This Mines Model is a model of the physical and administrative characteristics of mines. It considers a mine to be both a geospatial object (a special type of man-made Feature) with spatial properties and relations and also a conceptual object with properties for operation such, as agents with roles like "Operator", the project that manages the mine and legislative or regulatory instrument relations, to things such as Permits.

## Modelling Principles

### Site & Mine Typing

A _Site Types_ vocabulary defines the various specialised types of Site, such as _Mine_, _Infrastructure_, _Processing Plant_ etc. and, within that, there is a hierarchy of types narrower than _Mine_. Object of the class Mine in this model may onl be further typed with narrower concepts of _Mine_. 

### Agent Relations

<a href="../../assets/mines-Agents.svg">
<figure id="figure-bh" markdown style="width:50%">
  ![](../assets/mines-Agents.svg)
  <figcaption>Figure MO: Mines Model Agent relations - general pattern</figcaption>
</figure>
</a>

Agents relations - of Mines and Mine Projects to People and Organisations - follows the standards [PROV](../background.md#prov) standard [_qualified relations pattern_](https://www.w3.org/TR/prov-o/#cross-reference-qualified-terms) so Agents with relations to Mines and Projects can be indicated with Roles. the following example uses both the un-qualified and qualified relations above for a fictitious Mine, Project and Permit. 

### Authorities

<a href="../../assets/mines-Authorities.svg">
<figure id="figure-bh" markdown style="width:70%">
  ![](../assets/mines-Authorities.svg)
  <figcaption>Figure MO: Mines Authorities</figcaption>
</figure>
</a>

### Commodities

<a href="../../assets/mines-Commodities.svg">
<figure id="figure-bh" markdown style="width:60%">
  ![](../assets/mines-Commodities.svg)
  <figcaption>Figure MO: Mines Commodities</figcaption>
</figure>
</a>

## Example Scenarios

## Example Data

## Vocabularies

