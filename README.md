## A standardisation framework for bio-logging data
This repository contains a standardisation framework for bio-logging data proposed by Sequeira et al (in prep for submission to Nature Scientific Data) and involving data flow from manufacturers and researchers to compliant repositories. The objective of adopting this framework is to standardise bio-logging data to promote efficient data collation, usage, and sharing.

### [Templates](templates)
The framework includes the use of three templates, which can be found in the templates folder, each specifying how to format all data and metadata needed. Inside the templates folder you can also find a [templates.md](templates/templates.md) file providing a brief description of the three templates:
-	the [device-metadata.md](templates/device-metadata.md) containing all information pertaining to the bio-logging instrument used to collect data,
-	the [deployment-metadata.md](templates/deployment-metadata.md) containing all information pertaining to the attachment of the bio-logging device to the animal (i.e., deployment procedure), and
-	the [input-data.md](templates/input-data.md) containing all bio-logging data collected by one deployment of the bio-logging device
All three templates include definitions for each attribute name and links to other similar terms used in other vocabularies, as well as SensorML and DarwinCore examples so they can be readily used by manufacturers and researchers alike.
Inside the Templates folder you can also find a [Fields](templates/fields) folder, including all the details from all fields used in the three templates.

### [Examples](examples/braun-blueshark)
The framework includes the description of an automated procedure to be created at the compliant repositories to translate ingested data and metadata into four levels of data standardisation. The objective of this step is to maximize interoperability and facilitate scientific discovery, conservation management, and policy development.
This automated procedure and the four data levels are exemplified in the [examples](examples/braun-blueshark) folder using a blue shark dataset ([Braun et al 2019, PNAS]), and include:
-	[Blue-shark-standardisation.md](examples/braun-blueshark/Blue-shark-standardization.md): automated procedure to translate data from level 1 to level 4
- [Blue-shark-standardisation.Rmd](examples/braun-blueshark/Blue-shark-standardisation.Rmd): automated procedure to translate data from level 1 to level 4 in R
- [braun_blues_deployment-metadata.csv](examples/braun-blueshark/braun_blues_deployment-metadata.csv): Example of a filled deployment metadata template for the example data provided here
- [braun_blues_device-metadata.csv](examples/braun-blueshark/braun_blues_device-metadata.csv): Example of a filled device metadata template for the example data provided here
-	[data-level1](examples/braun-blueshark/data-level1): Formatted decoded sensor data, i.e., decrypted low-level information obtained directly from sensors after decoding data collected.
-	[data-level2](examples/braun-blueshark/data-level2): Curated bio-logging data, i.e., a quality-controlled dataset after removal of invalid, inconsistent or erroneous data points.
-	[data-level3](examples/braun-blueshark/data-level3): Interpolated data, i.e., processed bio-logging data that includes smoothed and interpolated locations.
-	[data-level4](examples/braun-blueshark/data-level4): Gridded data, i.e., bio-logging data presented in a grid format with a specific grid-cell size and temporal resolution.
-	[sensorml-example](examples/braun-blueshark/sensorml-example): a SensorML example for the device used in the blue shark dataset
Our objective is to contribute to standardising bio-logging datasets across all taxa and ecosystems, which is one of the stated goals of the [International Bio-Logging Society](www.bio-logging.net "Bio-logging Society's homepage").
-	[wildlife_computers_raw](examples/braun-blueshark/wildlife_computers_raw): Original decoded sensor data provided by the manufacturer. Translation of these decoded data into Level 1 format is provided in the [Blue-shark-standardisation.md](examples/braun-blueshark/Blue-shark-standardisation.md) example.

### Questions?
* You can use the "issues" tab to ask new questions
* Please do so only after confirming there are no similar questions being addressed

### Would you like to contribute?
* You can use “pull requests” to suggest changes
* Please contact us here

### License
[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0)
