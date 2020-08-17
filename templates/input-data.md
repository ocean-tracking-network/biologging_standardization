## Table S3. Input data template 

Data fields provided by the researcher upon submission of data to repository (i.e. column headers). Alongside the completed Device Metadata table and Deployment Metadata table (linked by DeploymentID), this completes the submission to the repository. (CLS = Collecte Localisation Satellites)

| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [instrumentID](fields/instrumentID.md) | Unique instrument ID. Can be the instrument serial number, or other similar identification system used by the manufacturer.| | alpha-numerical, e.g. “09A0178”|
| [deploymentID](fields/deploymentID.md) | Unique identifier for single deployment of device. |  | |
| [organismID](fields/organismID.md) | Unique identifier for an individual, links data from different deployments or instruments on the same animal. |  | |
| [organismIDSource](fields/organismIDSource.md) | URN denoting the globally unique identifier as assigned by the repository publishing the dataset. |  | urn:catalog:[repository]:[institution]:[projectcode]:[OrganismID], e.g. urn:catalog:otn:Dalhousie:NSBS:Brandy|

| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [time](fields/time.md) | Timestamp of data point. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”|
| [latitude](fields/latitude.md) | Latitude of data point. | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|
| [longitude](fields/longitude.md) | Longitude of data point. | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|
| [argosLC](fields/argosLC.md) | Argos quality class for positions retrieved from ARGOS. | CLS Argos  | Categorical (G,3,2,1,0,A,B,Z)|
| [argosFilterMethod](fields/argosFilterMethod.md) | Filter method implemented by CLS/Argos to generate location. | CLS Argos  | Categorical: Least squares or Kalman|
| [argosErrorRadius](fields/argosErrorRadius.md) | Error radius for location provided by CLS/Argos. | CLS Argos  | meters|
| [argosSemiMajor](fields/argosSemiMajor.md) | Length of semi-major axis of error ellipse provided by CLS/Argos. Defaults to NA if Least-Squares Data. | CLS Argos  | meters|
| [argosSemiMinor](fields/argosSemiMinor.md) | Length of semi-minor axis of error ellipse provided by CLS/Argos. Defaults to NA if Least-Squares Data. | CLS Argos  | meters|
| [argosOrientation](fields/argosOrientation.md) | Orientation of error ellipse provided by CLS/Argos. | CLS Argos  | degrees from North (heading east)|
| [argosGDOP](fields/argosGDOP.md) | Geometric Dilution of Precision provided by CLS/Argos. | CLS Argos  | m/Hz|
| [gpsSatelliteCount](fields/gpsSatelliteCount.md) | The number of satellites used to estimate location (rapid acquisition GPS). |  | numerical e.g. “4”|
| [residualsGPS (rapid acquisition GPS)](fields/residualsGPS.md) | Measure of how well the solution provided for the location estimate matched the observed data. |  | Numerical e.g. "45.5" |
| [temperatureGLS](fields/temperatureGLS.md) | In situ temperature measured by instrument (can be used to correct geolocation positions). Associated with depth in "Depth GLS". |  | numerical in °C|
| [depthGLS](fields/depthGLS.md) | Depth of the in situ temperature measurements taken and recorded in "Temperature GLS" field.  |  |numerical in m |
| [sensorIType](fields/sensorIType.md) | Type of sensor contained in tag (e.g. pressure sensor, thermistor, induction cell) from Device metadata table. Can be repeated for any number of sensors (N), with Roman numeral representing sensor number (e.g. SensorI, SensorII...SensorN). |  | Categorical. Must reference one-to-one to a sensor type listed in Device metadata table.|
| [sensorIMeasurement](fields/sensorIMeasurement.md) | Measurement taken by SensorI at this time and location. Can be repeated for any number of sensors (N), as specified in Device template (e.g. SensorI, SensorII,...SensorN). Units of measurement and other relevant metadata documented in Device metadata table. |  | Unit as specified in Device metadata table for this sensor|
