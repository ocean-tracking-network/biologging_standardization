## Table S2. Deployment metadata template 

Deployment information including instrument settings, organism metadata, and tagging procedures. The Deployment metadata template is to be completed by the researcher and uploaded to a compliant repository alongside the data, as well as the Device metadata template provided by the manufacturer. All attributes are mandatory, but fields can be “unknown” or “NA” if data do not exist or are not applicable. Organism mass and size measurement fields can be repeated to provide additional measurements applicable to the taxon (e.g. for a shark: pre-caudal length, fork length, total length; for a pinniped: standard length, curve length, axillary girth; for a turtle: curved carapace length).

ITIS = Integrated Taxonomic Information System (https://www.itis.gov/)
CF = Climate and Forecast Metadata Conventions 
ACDD = Attribute Conventions for Data Discovery
ISO = International Organization for Standardization (https://www.itis.gov/)

| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [DeploymentID](fields/deploymentID.md) | Unique identifier for single deployment of device. |  | |

### Instrument metadata
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [InstrumentID](fields/instrumentID.md) | Unique instrument ID. Can be the instrument serial number, or other similar identification system used by the manufacturer. |  | alpha-numerical, eg. “09A0178”|
| [PTT](fields/ptt.md) | Platform Transmitter Terminal for Argos transmission. |  | numerical, eg. “178937”|
| [Owner name](fields/ownerName.md) | Name of person to contact regarding the deployment. |  | String containing full name|
| [Owner email contact](fields/ownerEmailContact.md) | Email contact for person indicated under ‘Owner name’. |  | String containing e-mail|
| [Owner institutional contact](fields/ownerInstitutionalContact.md) | Institutional address for person indicated under ‘Owner name’. |  | String containing institutional address|
| [Owner phone contact](fields/ownerPhoneContact.md) | Phone contact for person indicated under ‘Owner name’. |  | String containing contact phone|
| [License](fields/license.md) | Terms of use for the data in the study, provided by the study owner. If no license terms are specified by researcher, the General repository Terms of Use apply.|  | Categorical|
| [Transmission settings](fields/transmissionSettings.md) | Step duration and location uplink limit (can add rows if needed) |  | String with duration in hours, followed by number of messages e.g. “24 hours, 200 messages”|
| [Transmission mode](fields/transmissionMode.md) | User-defined conditions for entering and exiting Haul-Out mode (slower repetition rate) and transmission control in Haul-Out if applicable |  | Time settings in minutes e.g. “Haul-Out state entered after 10 consecutive dry minutes (40 seconds/minute), exited if wet for 30 seconds/minute” OR “disabled”|
| [Duty cycle](fields/dutyCycle.md) | Detailed instrument settings defined in a file (e.g. Wildlife Computers Report, htm file/URL, or screenshot of tag settings). |  | String in sentence, e.g. PTT active 12 hours, followed by 6 hours sleep-mode|
| [Instrument Settings](fields/instrumentSettings.md) | Attach a file with detailed instrument settings (eg. Wildlife Computers Report .htm file or screenshot of tag settings). |  | File (.htm, .pdf)|

### Organism metadata
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [OrganismID](fields/organismID.md) | Unique identifier for an individual, link data from different deployments or instruments on the same animal. |  | Alpha-numerical|
| [OrganismID source](fields/organismIDSource.md) | URN denoting the authority from which the species identification is defined. |  | e.g. EXAMPLE|
| [Scientific name](fields/scientificName.md) | Binomial species name of organism carrying instrument. | ITIS | String of the format “Genus species”, genus capitalized, separated by one space, eg. “Mirounga angustirostris”|
| [Common name](fields/commonName.md) | One or more common name(s) of organism carrying instrument. |  | String in sentence case, separated by space|
| [Organism sex](fields/organismSex.md) | Sex of organism carrying instrument. |  | Categorical: M, F, U|
| [Organism mass](fields/organismMass.md) | Mass of organism carrying instrument (can be repeated for multiple mass measurements). |  | numerical in kg|
| [Organism mass measurement details](fields/organismMassMeasurementDetails.md) | Situation when the animal mass was taken (e.g., at instrument deployment, instrument recovery, recapture).
 |  | Categorial: Deployment, Recovery, Other|
| [Organism mass measurement time](fields/organismMassMeasurementTime.md) | Date when the organism mass was taken of animal mass | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”|
| [Organism size](fields/organismSize.md) | Size of organism carrying instrument (can be repeated for multiple measurements). |  | numerical in m or unknown|
| [Organism size measurement type](fields/organismSizeMeasurementType.md) | Type and description of method used for size measurement reported |  | String, e.g. total length (from shark snout to top tip of tail)|
| [Organism size measurement time](fields/organismSizeMeasurementTime.md) | When the organism size measurement was taken |  | Categorial: Deployment, Recovery, Other|
| [Organism age class/reproductive class](fields/organismAgeReproductiveClass.md) | Age class of organism carrying instrument at the time the instrument was attached |  | Categorical: ad, juv, unk|
| [Attachment method ](fields/attachmentMethod.md) | Method with which instrument was attached |  | String, eg. “anchor”|
| [Deployment date and time](fields/deploymentDateTime.md) | Timestamp the instrument was deployed on the organism | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”|

### Movement metadata
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [Deployment latitude](fields/deploymentLatitude.md) | Latitude in decimal degrees of instrument deployment | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|
| [Deployment longitude](fields/deploymentLongitude.md) | Longitude in decimal degrees of instrument deployment. | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|
| [Detachment date and time](fields/detachmentDateTime.md) | Timestamp the instrument was recovered or otherwise detached from the organism (if known). | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”|
| [Detachment details](fields/detachmentDetails.md) | Brief description of recovery/detachment if known (e.g., caught in fisheries, recaptured animal, predetermined detachment). |  | String in sentence case (e.g., caught in fisheries)|
| [Latitude of detachment](fields/detachmentLatitude.md) | Latitude in decimal degrees of instrument recovery/detachment from organism (if known). | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|
| [Longitude of detachment](fields/detachmentLongitude.md) | Longitude in decimal degrees of instrument recovery/detachment from organism (if known). | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|
| [Track start time](fields/trackStartTime.md) | Timestamp at which organism track starts if different from deployment time. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”|
| [Track start latitude](fields/trackStartLatitude.md) | Latitude at which track of organism begins (may or may not be different from deployment latitude) | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|
| [Track start longitude](fields/trackStartLongitude.md) | Longitude at which track of organism begins (may or may not be different from deployment longitude). | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|
| [Track end time](fields/trackEndTime.md) | Timestamp at which track of organism ends | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”|
| [Track end latitude](fields/trackEndLatitude.md) | Latitude at which organism track ends. | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|
| [Track end longitude](fields/trackEndLongitude.md) | Longitude at which organism track ends. | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|
| [Deployment End Type](fields/deploymentEndType.md) | Classification of instrument deployment end. | Movebank | Categorical (eg. removal, equipment failure, fall off)|
| [Sun angle (GLS)](fields/sunangleGLS.md) | Angle of the sun to determine twilight derived at the beginning of deployment. | | Numerical in degrees


### Environmental data calibration
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [Calibrations done](fields/calibrationsDone.md) | Provide link to calibration file |  | DOI or URL|
| [QC done by](fields/qcDoneBy.md) | Provide name of the person who performed quality control |  | string|
| [QC problems found](fields/qcProblemsFound.md) | Data quality problem(s) detected |  | Y/N|
| [QC notes](fields/qcNotes.md) | Description of QC done, eg. “temperatures outside of xx range removed”, number of cases flagged |  | text field|

### Physiological data calibration
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [Calibrations done](fields/calibrationsDone.md) | Provide link to calibration file |  | DOI or URL|
| [QC done by](fields/qcDoneBy.md) | Provide name of the person who performed quality control |  | string|
| [QC problems found](fields/qcProblemsFound.md) | Data quality problem(s) detected |  | Y/N|
| [QC notes](fields/qcNotes.md) | Description of QC done, eg. codes used, # of cases flagged, description of problem |  | text field|

### Accelerometry data calibration
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [Position of accelerometer on organism](fields/positionOfAccelerometerOnOrganism.md) | Where the accelerometer was placed on the organism and its orientation if applicable |  | string, eg. “head”|
| [Calibrations done](fields/calibrationsDone.md) | Provide link to calibration file |  | DOI or URL|
| [QC done by](fields/qcDoneBy.md) | Provide name of the person who performed quality control |  | string|
| [QC problems found](fields/qcProblemsFound.md) | Data quality problem(s) detected |  | Y/N|
| [QC notes](fields/qcNotes.md) | Description of QC done, eg. codes used, # of cases flagged, description of problem |  | text field|

### Other data
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [Other relevant identifiers](fields/otherRelevantIdentifiers.md) | Other identifiers relevant to deployment (eg. WMO number for data contribution to GTS) |  | |
| [Other data types associated with deployment](fields/otherDataTypesAssociatedWithDeployment.md) | Additional data collected with instrument deployment, eg. from ancillary sensors |  | string, eg. “light level”|
| [Other data co-owners](fields/otherDataCoowners.md) | Names of additional people to acknowledge for data |  | |
| [References](fields/references.md) | Published or web-based references that describe the data or methods |  | DOI or URL|

