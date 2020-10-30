## A standardisation framework for bio-logging data
This repository contains a standardisation framework for bio-logging data proposed by Sequeira et al<sup>1</sup> (submitted to Methods in Ecology and Evolution) and involving data flow from manufacturers and researchers to compliant repositories. The objective of adopting this framework is to standardise bio-logging data to promote efficient data collation, usage, and sharing.

### [Templates](templates)
The framework includes the use of three templates outlining the events that generate bio-logging data and metadata, and the exact details that must be captured from these events to produce an optimally reuseable and generalizable animal movement data product. The names and descriptions of the required fields in this set of templates can be found in the templates folder of this repository. A descriptive page has been created for each variable, specifying how to format each entry and the controlled vocabularies that are acceptable to use. Inside the templates folder you can also find a [templates.md](templates/templates.md) file providing a brief overview of the three templates as a whole:
-	the [device-metadata.md](templates/device-metadata.md) containing all information pertaining to the bio-logging instrument used to collect data,
-	the [deployment-metadata.md](templates/deployment-metadata.md) containing all information pertaining to the attachment of the bio-logging device to the animal (i.e., deployment procedure), and
-	the [input-data.md](templates/input-data.md) containing all bio-logging data collected by one deployment of the bio-logging device
All three templates include definitions for each attribute name and links to other similar terms used in other vocabularies, including examples in SensorML and DarwinCore  so they can be readily used by manufacturers and researchers alike.
Inside the Templates folder you can also find a [Fields](templates/fields) folder, including all the details from all fields used in the three templates.

### Controlled Vocabularies
For biologically-sourced terms, we recommend a specific field in the [Darwin Core (DwC)](https://dwc.tdwg.org/) standard. Any terms that are biological in nature that are not covered by this framework can and should be included, with the appropriate Darwin Core name and content.
For sensor-based information obtained from instrument manufacturers, we have made examples to conform with in [Sensor Model Language](https://www.ogc.org/standards/sensorml)
For all other researcher and manufacturer provided fields, we recommend first using the [Climate and Forecast](https://cfconventions.org/index.html) vocabularies.

### [Examples](examples/braun-blueshark)
The framework includes the description of an automated procedure to be created at the compliant repositories to translate ingested data and metadata into four levels of data standardisation. The objective of this step is to maximize interoperability and facilitate scientific discovery, conservation management, and policy development.
This automated procedure and the four data levels are exemplified in the [examples](examples/braun-blueshark) folder using a blue shark dataset ([Braun et al 2019, PNAS](https://www.pnas.org/content/116/35/17187)), and include:
-	[Blue-shark-standardisation.md](examples/braun-blueshark/Blue-shark-standardization.md): automated procedure to translate data from level 1 to level 4
- [Blue-shark-standardisation.Rmd](examples/braun-blueshark/Blue-shark-standardization.Rmd): automated procedure to translate data from level 1 to level 4 in R
- [braun_blues_deployment-metadata.csv](examples/braun-blueshark/braun_blues_deployment-metadata.csv): Example of a filled deployment metadata template for the example data provided here
- [braun_blues_device-metadata.csv](examples/braun-blueshark/braun_blues_device-metadata.csv): Example of a filled device metadata template for the example data provided here
-	[data-level1](examples/braun-blueshark/data_level1/): Formatted decoded sensor data, i.e., decrypted low-level information obtained directly from sensors after decoding data collected.
-	[data-level2](examples/braun-blueshark/data_level2/): Curated bio-logging data, i.e., a quality-controlled dataset after removal of invalid, inconsistent or erroneous data points.
-	[data-level3](examples/braun-blueshark/data_level3/): Interpolated data, i.e., processed bio-logging data that includes smoothed and interpolated locations.
-	[data-level4](examples/braun-blueshark/data_level4): Gridded data, i.e., bio-logging data presented in a grid format with a specific grid-cell size and temporal resolution.
-	[sensorml-example](examples/braun-blueshark/sensorml-example): a SensorML example for the device used in the blue shark dataset
- [darwincore-example](examples/braun-blueshark/darwincore-example): a Darwin Core example showing how the blue shark dataset can easily be converted to Darwin Core
-	[wildlife_computers_raw](examples/braun-blueshark/wildlife_computers_raw): Original decoded sensor data provided by the manufacturer. Translation of these decoded data into Level 1 format is provided in the [Blue-shark-standardisation.md](examples/braun-blueshark/Blue-shark-standardization.md) example.

Our objective is to contribute to standardising bio-logging datasets across all taxa and ecosystems, which is one of the stated goals of the [International Bio-Logging Society](https://www.bio-logging.net "Bio-logging Society's homepage").

### Rationale

Since the inception of electronic animal tracking, many research networks and data assimilation initiatives (OTN, IMOS, ATN, SAIAB, MigraMar, TOPP, TAG) have worked to better aggregate and publish electronically-derived marine animal movement data. Their efforts have cumulated in a handful of network-wide standards that can be now aggregated and adapted to a single global framework for publishing and expressing animal movement data at various useful scales. The unification of the significant output from these networks will be a data resource unmatched in size and scope, made available in a common, digestible format that will prove valuable across initiatives such as GOOS's [Biological Essential Ocean Variables](http://www.goosocean.org/biology), the [Marine Megafauna Movement Analytical Program](https://mmmap.wordpress.com/) now called MegaMove, [Migratory Connectivity in the Ocean](https://mico.eco/), the [Global Shark Movement Project](https://www.globalsharkmovement.org/), the IOC's [Ocean Biodiversity Information System](https://obis.org), and the Group on Earth Observations Biodiversity Observation Network's [Essential Biodiversity Variables](https://geobon.org/ebvs/what-are-ebvs/). By providing sensible and traceable aggregations across a wide range of animal tracking data, we give networks as well as the individual researchers who are behind them an attainable data formatting target that will allow their data to join any and all of these aspects of our global understanding of how animals are using the ocean.

### Questions?
* You can use the "issues" tab to ask new questions
* Please do so only after confirming there are no similar questions being addressed

### Would you like to contribute?
* You can use “pull requests” to suggest changes
* Please contact us here

### License
[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0)


<sup>1</sup>Ana M.M. Sequeira, Malcolm O’Toole, Theresa R. Keates, Laura H. McDonnell, Camrin D. Braun, Xavier Hoenner, Fabrice R. A. Jaine, Ian D. Jonsen, Peggy Newman, Jonathan Pye, Steven J. Bograd, Graeme C. Hays, Elliott L Hazen, Melinda Holland, Vardis Tsontos, Clint Blight, Francesca Cagnacci, Sarah C. Davidson, Holger Dettki, Carlos M. Duarte, Daniel C. Dunn, Victor M. Eguíluz, Michael Fedak, Adrian C. Gleiss, Neil Hammerschlag, Mark A. Hindell, Kim Holland, Ivica Janekovic, Megan K. McKinzie, Mônica M.C.Muelbert, Chari Pattiaratchi, Christian Rutz, David W. Sims, Samantha E. Simmons, Brendal Townsend, Frederick Whoriskey, Bill Woodward, Daniel P. Costa, Michelle R. Heupel, Clive R. McMahon, Rob Harcourt, Michael Weise. __A standardisation framework for bio-logging data to advance ecological research and conservation__. Submitted to *Methods in Ecology and Evolution*.
