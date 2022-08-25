# GSWA Supermodel

This repository contains the source code for the website documenting the [Geological Survey of Western Australia](https://dmp.wa.gov.au/Geological-Survey/Geological-Survey-262.aspx) within the [Department of Mines, Industry Regulation and Safety](https://www.dmirs.wa.gov.au).

Please see the documentation's online location:

* blah

## License & Rights

This repository's content is available for reuse according to the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

This content is copyright as follows:

&copy; Government of Western Australia, 2022

## Contacts

For technical matters, please contact:

**Nicholas Car**  
_Geoscience Data Architect_  
Geological Survey of WA  
Department of Mines, Industry Regulation and Safety  
<nick.car@dmirs.wa.gov.au>

For other matters, please contact:

**Geological Survey of Western Australia**  
<https://dmp.wa.gov.au/Geological-Survey/Geological-Survey-262.aspx>

# Technical Operations

This repository uses the [MkDocs](https://www.mkdocs.org/) tool to build a static website - just HTML pages, no database etc. - from simple [Markdown](https://www.markdownguide.org/) text files and images.

MkDocs uses [Python](https://www.python.org/) scripting to compile the Markdown files, images etc. into HTML. It can be run locally - on a desktop/laptop - to test documentation changes, and pushed to GitHub to be auto-deployed.

To serve this content as a static site locally, run:

`mkdocs serve`