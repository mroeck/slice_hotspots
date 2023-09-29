# slice_hotspots
Pre-release version (230921)
* SLiCE Building Data Model Article (Preprint) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8369244.svg)](https://doi.org/10.5281/zenodo.8369244)
* SLiCE Hotspot Analysis Tool (this repo) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8366478.svg)](https://doi.org/10.5281/zenodo.8366478)
Latest version: Available via https://github.com/mroeck/slice_hotspots/tree/main (main)


# Hotspot Analysis Tool
This repository offers a tool for systematic analysis of environmental hotspots across the life cycle of buildings and construction elements using data compliant with the SLiCE building data model.

## Protocol
The basis for the environmental hotspot analysis routine and prototype implementation presented here are the EF hotspot analysis protocol developed by [11] and experiences from its application within the PEF4Buildings project [12–14]. A summary of the hotspot analysis methodology [11] and specificities of this implementation is offered in Table 1 and elaborated in the following. In this implementation, the hotspot analysis protocol follows a three-step procedure, which involves identifying the most relevant indicators (e.g., impact categories), temporal hotspots (e.g., life cycle stages), and spatial hotspots (e.g., materials, processes and/or elementary flows).

## Prototype
The SLiCE hotspots tool enables the analysis of environmental hotspots within building assessment results following the SLiCE data model – see Figure 8 for a conceptual overview of the tool, based on snippets of the current prototype of the tool, implemented via JupyterNotebook [36] and Panel [25].

To start, the hotspot analysis script requires some user inputs and settings:

1. First, a SLiCE-compliant dataset as well as a file with weighting factors related to the impact indicators in the dataset have to be specified.
2. Second, the ‘level 0’ attribute object must be specified, which represents the baseline for the analysis and determines the attribute value(s) that can be selected for inclusion in the analysis. Depending on whether one or more items (attribute values) are selected, the results will provide insights on one item and its hotspots or allow for comparison of different items.
3. Third, the indicators to be considered in the hotspot analysis must be selected. These will be normalised and weighted to obtain a common base unit, based on the weighting factors/sets which also must be selected here (if several weighting sets are available, including an option of “equal weighting”). Here it is furthermore possible to unselect indicators or select just one, in which case the consecutive steps of the analysis will only consider the active indicators.
4. Fourth, the temporal attribute is defined, i.e., the attribute based on which the most relevant life cycle stages will be determined. The selection mask allows to select one or many life cycle stages, with all stages selected by default. Here it is possible to focus the analysis on selected life cycle stages, for example, to assess the most relevant indicators, life cycle stages and processes within the building use-phase, or for embodied impacts only.
5. Fifth, the ‘level -1’ attribute is specified, which represents the ‘process’ level in this analysis. The SLiCE tool is flexible with regards to defining ‘level-1’ as any spatial level below the initial ‘level0’ attribute. This means, for example, if ‘level0’ is the ‘building level’, then ‘level-1’ can be ‘building element’, ‘work section’, or ‘material level’, respectively.
6. Sixth, the threshold value for the cumulative impact of ‘most relevant’ items is defined. By default, it is set at 80%, as per the PEF/OEF hotspot analysis protocol, but can be changed as needed.
7. Lastly, when the above settings have been defined (or changed), pushing the ‘Run hotspot analysis’ button will run the analysis and generate (or updated) results tables and plots.

For further information on the SLiCE building data model please review the related article (linked below)


# Software and data availability
The SLiCE building data model as well as the presented implementation in the SLiCE hotspot analysis prototype are open source and available with this article. The SLiCE hotspot analysis, implemented as an IPython Jupyer Notebook with interactive widgets, tool is available on Github (https://github.com/mroeck/slice_hotspots/), with the submission pre-release published via Zenodo (https://zenodo.org/badge/latestdoi/645859866). All items are published under a GNU General Public License v3.0. We encourage you to review, reuse, and refine the model and scripts and share-alike.


# Contributing
The SLiCE Building Data Model and the SLiCE hotspot analysis tool are intended for collaborative use and joint future devleopment.  We need your active contributions to further improve and grow the open building data and tools landscape. Reach out to the lead author (email, linkedin) if you are interested to contribute.


# Preprint (not peer-reviewed)
Röck M, Passer A, Allacker K. “SLiCE: An Open Data Model for Scalable High-Definition Life Cycle Engineering, Hotspot Analysis and Dynamic Assessment of Buildings.” 2023, Preprint DOI: https://doi.org/10.5281/zenodo.8369244


# Cite as
When referring to this work, please cite both the data model and the tool:
* SLiCE Building Data Model (Preprint): RÖCK, Martin, PASSER, Alexander, & ALLACKER, Karen. (2023). SLiCE: An Open Data Model for Scalable High-Definition Life Cycle Engineering, Hotspot Analysis and Dynamic Assessment of Buildings. Zenodo. https://doi.org/10.5281/zenodo.8369244
* SLiCE Hotspot Analysis Tool (Pre-release): RÖCK, Martin, PASSER, Alexander, & ALLACKER, Karen. (2023). mroeck/slice_hotspots: Pre-release (0.1.1). Zenodo. https://doi.org/10.5281/zenodo.8366478
