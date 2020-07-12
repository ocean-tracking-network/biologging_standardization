## Table S2. Deployment metadata template 

Deployment information including instrument settings, organism metadata, and tagging procedures. The Deployment metadata template is to be completed by the researcher and uploaded to a compliant repository alongside the data, as well as the Device metadata template provided by the manufacturer. All attributes are mandatory, but fields can be “unknown” or “NA” if data do not exist or are not applicable. Organism weight can be measured at instrument deployment and remeasured once if applicable; up to three size measurement fields can be reported  (e.g. for a shark: pre-caudal length, fork length, total length; for a pinniped: standard length, curve length, axillary girth; for a turtle: curved carapace length).

ITIS = Integrated Taxonomic Information System (https://www.itis.gov/)
CF = Climate and Forecast Metadata Conventions 
ACDD = Attribute Conventions for Data Discovery
ISO = International Organization for Standardization (https://www.itis.gov/)

| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [deploymentID](fields/deploymentID.md) | Unique identifier for single deployment of device. |  | |

### Instrument metadata
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [instrumentID](fields/instrumentID.md) | Unique instrument ID. Can be the instrument serial number, or other similar identification system used by the manufacturer. |  | alpha-numerical, eg. “09A0178”|	
| [ptt](fields/ptt.md) | Platform Transmitter Terminal for Argos transmission. |  | numerical, eg. “178937”|		
| [transmissionSettings](fields/transmissionSettings.md) | Step duration and location uplink limit (can add rows if needed) |  | String with duration in hours, followed by number of messages e.g. “24 hours, 200 messages”|	
| [transmissionMode](fields/transmissionMode.md) | User-defined conditions for entering and exiting power-saving mode (i.e. slower sampling rate) and transmission control, if applicable. |  | Time settings in minutes e.g. “Haul-Out state entered after 10 consecutive dry minutes (40 seconds/minute), exited if wet for 30 seconds/minute” OR “disabled”|	
| [dutyCycle](fields/dutyCycle.md) | Detailed instrument settings defined in a file (e.g. Wildlife Computers Report, htm file/URL, or screenshot of tag settings). |  | String e.g. "PTT active 12 hours, followed by 6 hours sleep-mode"|
| [instrumentSettings](fields/instrumentSettings.md) | Attach a file with detailed instrument settings (eg. Wildlife Computers Report .htm file or screenshot of tag settings). |  | File (.htm, .pdf)|		

### Movement metadata
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [deploymentDateTime](fields/deploymentDateTime.md) | Timestamp the instrument was deployed on the organism. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”| 
| [deploymentLatitude](fields/deploymentLatitude.md) | Latitude in decimal degrees of instrument deployment. | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|   
| [deploymentLongitude](fields/deploymentLongitude.md) | Longitude in decimal degrees of instrument deployment. | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|   
| [deploymentEndType](fields/deploymentEndType.md) | Classification of instrument deployment end, i.e. what ended teh collection of usable data, which may or may not be tag removal. | Movebank | Categorical (eg. removal, equipment failure, fall off)|
| [detachmentDateTime](fields/detachmentDateTime.md) | Timestamp the instrument was recovered or otherwise detached from the organism (if known). | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”| 
| [detachmentDetails](fields/detachmentDetails.md) | Brief description of recovery/detachment if known (e.g., caught in fisheries, recaptured animal, predetermined detachment). |  | String in sentence case (e.g., caught in fisheries)|
| [detachmentLatitude](fields/detachmentLatitude.md) | Latitude in decimal degrees of instrument recovery/detachment from organism (if known). | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|   
| [detachmentLongitude](fields/detachmentLongitude.md) | Longitude in decimal degrees of instrument recovery/detachment from organism (if known). | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|   
| [trackStartTime](fields/trackStartTime.md) | Timestamp at which organism track starts if different from deployment time. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”| 
| [trackStartLatitude](fields/trackStartLatitude.md) | Latitude at which track of organism begins (may or may not be different from deployment latitude). | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|   
| [trackStartLongitude](fields/trackStartLongitude.md) | Longitude at which track of organism begins (may or may not be different from deployment longitude). | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|   
| [trackEndTime](fields/trackEndTime.md) | Timestamp at which track of organism ends. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”| 
| [trackEndLatitude](fields/trackEndLatitude.md) | Latitude at which organism track ends. | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|   
| [trackEndLongitude](fields/trackEndLongitude.md) | Longitude at which organism track ends. | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|   
| [sunElevationAngle](fields/sunElevationAngle.md) | Angle of the sun to determine twilight derived at the beginning of deployment. | | Numerical in degrees  

### Organism metadata
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [organismID](fields/organismID.md) | Unique identifier for an individual, link data from different deployments or instruments on the same animal. |  | Alpha-numerical|   
| [organismIDSource](fields/organismIDSource.md) | URN denoting the authority from which the species identification is defined. |  | urn:catalog:[repository]:[institution]:[projectcode]:[OrganismID], e.g., urn:catalog:otn:Dalhousie:NSBS:Brandy-release| 
| [scientificName](fields/scientificName.md) | Binomial species name of organism carrying instrument. | | String of the format “Genus species”, genus capitalized, separated by one space, e.g. “Mirounga angustirostris”|  
| [scientificNameSource](fields/scientificNameSource.md) | URN denoting the authority from which the species identification is defined | ITIS / WoRMS / other | free-text, e.g. for 'blue shark': urn:lsid:marinespecies.org:taxname:105801, TSN 160424 , (Linnaeus, 1758)|
| [commonName](fields/commonName.md) | One or more common name(s) of organism carrying instrument. |  | String in sentence case, separated by space|   
| [organismSex](fields/organismSex.md) | Sex of organism carrying instrument. |  | Categorical: M, F, U| 
| [organismWeightAtDeployment](fields/organismWeightAtDeployment.md) | Weight of organism carrying instrument measured at tag deployment. |  | numerical in kg|  
| [organismWeightRemeasurement](fields/organismWeightRemeasurement.md) | Weight of organism carrying instrument at another time (specified in "Organism weight re-measurement time") than deployment.|  | numerical in kg|  
| [organismWeightRemeasurementTime](fields/organismWeightRemeasurementTime.md) | Timestamp when the additional measurement of organism weight was taken. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”| 
| [organismSize](fields/organismSize.md) | Size of organism carrying instrument (can be repeated for up to three measurements). |  | numerical in m or unknown|  
| [organismSizeMeasurementType](fields/organismSizeMeasurementType.md) | Type of method used for size measurement reported. |  | String, e.g. "total length"|   
| [organismSizeMeasurementDescription](fields/organismSizeMeasurementDescription.md) | Description of method used for size measurement reported. |  | String, e.g. "from shark snout to top tip of tail"|   
| [organismSizeMeasurementTime](fields/organismSizeMeasurementTime.md) | Timestamp when the organism size measurement was taken. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”| 
| [organismAgeReproductiveClass](fields/organismAgeReproductiveClass.md) | Age class of organism carrying instrument at the time the instrument was attached. |  | Categorical: adu, sub, juv, new, unk|
| [trappingMethodDetails](fields/trappingMethodDetails.md) | Method used to trap the organism for instrumentation, or to deploy the instrument without trapping. | | String, eg.  "trapped with hand-net on nest in breeding colony", "tag attached with pole onto organism feeding on bait, from vessel"|
| [attachmentMethod](fields/attachmentMethod.md) | Method with which instrument was attached. |  | String, eg. “anchor”|  

### Environmental data calibration  
| attributeName | description | standard | format |   
| ------------- | ----------- | -------- | ------ |  
| [calibrationsDone](fields/calibrationsDone.md) | Provide link to calibration file. |  | DOI or URL|  
| [qcDone](fields/qcDone.md) | Whether quality control was performed. |  | Y/N|  
| [qcProblemsFound](fields/qcProblemsFound.md) | Whether data quality problem(s) were detected. |  | Y/N|  
| [qcNotes](fields/qcNotes.md) | Description of QC done, e.g. “temperatures outside of xx range removed”, number of cases flagged. |  | text field| 
  
### Physiological data calibration  
| attributeName | description | standard | format |   
| ------------- | ----------- | -------- | ------ |  
| [calibrationsDone](fields/calibrationsDone.md) | Provide link to calibration file. |  | DOI or URL|  
| [qcDone](fields/qcDone.md) | Whether quality control was performed. |  | Y/N|  
| [qcProblemsFound](fields/qcProblemsFound.md) | Whether data quality problem(s) were detected. |  | Y/N|  
| [qcNotes](fields/qcNotes.md) | Description of QC done, e.g. codes used, # of cases flagged, description of problem. |  | text field|  
  
### Accelerometry data calibration  
| attributeName | description | standard | format |   
| ------------- | ----------- | -------- | ------ |  
| [positionOfAccelerometerOnOrganism](fields/positionOfAccelerometerOnOrganism.md) | Where the accelerometer was placed on the organism. |  | string, e.g. “head”|   
| [orientationOfAccelerometerOnOrganism](fields/orientationOfAccelerometerOnOrganism.md) | The orientation of the accelertometer on the organism, if applicable. |  | string, e.g. “facing towards front of head” | 
| [calibrationsDone](fields/calibrationsDone.md) | Provide link to calibration file. |  | DOI or URL|  
| [qcDone](fields/qcDone.md) | Whether quality control was performed. |  | Y/N|  
| [qcProblemsFound](fields/qcProblemsFound.md) | Whether data quality problem(s) were detected. |  | Y/N|  
| [qcNotes](fields/qcNotes.md) | Description of QC done, e.g. codes used, # of cases flagged, description of problem. |  | text field|  
  
### Other data  
| attributeName | description | standard | format |   
| ------------- | ----------- | -------- | ------ |  
| [ownerName](fields/ownerName.md) | Name of person to contact regarding the deployment. |  | String containing full name|  
| [ownerEmailContact](fields/ownerEmailContact.md) | Email contact for person indicated under "Owner name". |  | String containing e-mail|  
| [ownerInstitutionalContact](fields/ownerInstitutionalContact.md) | Institutional address for person indicated under "Owner name". |  | String containing institutional address|  
| [ownerPhoneContact](fields/ownerPhoneContact.md) | Phone contact for person indicated under "Owner name". |  | String containing contact phone|  
| [license](fields/license.md) | Terms of use for the data in the study, provided by the study owner. If no license terms are specified by researcher, the General repository Terms of Use apply.|  | Categorical| 
| [otherRelevantIdentifiers](fields/otherRelevantIdentifiers.md) | Other identifiers relevant to deployment (e.g. WMO number for data contribution to GTS). |  | |  
| [otherDataTypesAssociatedWithDeployment](fields/otherDataTypesAssociatedWithDeployment.md) |Additional data collected with instrument deployment, e.g. from ancillary sensors, photo-ID 
| [references](fields/references.md) | Published or web-based references that describe the data or methods. |  | DOI or URL|  
