## Table S4. Input data template 

Data fields provided by the researcher upon submission of data to repository (i.e. column headers). Alongside the completed Device Metadata table and Deployment Metadata table (linked by DeploymentID), this completes the submission to the repository. (CLS = Collecte Localisation Satellites)

| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [InstrumentID](fields/instrumentID.md) | Unique instrument ID. Can be the instrument serial number, or other similar identification system used by the manufacturer.| | alpha-numerical, eg. “09A0178”|
| [DeploymentID](fields/deploymentID.md) | Unique identifier for single deployment of device. |  | |
| [OrganismID](fields/organismID.md) | Unique identifier for an individual, links data from different deployments or instruments on the same animal. |  | |

| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [Time](fields/time.md) | Timestamp of data point. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”|
| [Latitude](fields/latitude.md) | Latitude of data point. | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|
| [Longitude](fields/longitude.md) | Longitude of data point. | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|
| [Argos LC](fields/argosLC.md) | Argos location class of data point's position. | CLS Argos  | Categorial (G,3,2,1,0,A,B,Z)|
| [Argos Filter method](fields/argosFilterMethod.md) | Filter method implemented by CLS/Argos to generate location. | CLS Argos  | Categorial: Least squares or Kalman|
| [Argos Error Radius](fields/argosErrorRadius.md) | Error radius for location provided by CLS/Argos. | CLS Argos  | meters|
| [Argos semi major](fields/argosSemiMajor.md) | Length of semi-major axis of error ellipse provided by CLS/Argos. Defaults to NA if Least-Squares Data. | CLS Argos  | meters|
| [Argos semi minor](fields/argosSemiMinor.md) | Length of semi-minor axis of error ellipse provided by CLS/Argos. Defaults to NA if Least-Squares Data. | CLS Argos  | meters|
| [Argos orientation](fields/argosOrientation.md) | Orientation of error ellipse provided by CLS/Argos. | CLS Argos  | degrees from North (heading east)|
| [Argos GDOP](fields/argosGDOP.md) | Geometric Dilution of Precision provided by CLS/Argos. | CLS Argos  | m/Hz|
| [GPS satellite count](fields/gpsSatelliteCount.md) | The number of satellites used to estimate location (rapid acquisition GPS). |  | numerical eg. “4”|
| [Residuals (fast-acquisition GPS)](fields/residualsGPS.md) | Measure of how well the solution provided for the location estimate matched the observed data. |  | Numerical e.g. "45.5" |
| [Temperature (GLS)](fields/temperatureGLS.md) | iIn situ temperature measured by instrument (can be used to correct geolocation positions). Associated with depth in "Depth GLS". |  | numerical in °C|
| [Depth (GLS)](fields/depthGLS.md) | Depth of in situ temperature measurements in “Temperature GLS”.  |  |numerical in m |
| [Sensor I type](fields/sensorIType.md) | Type of sensor contained in tag (e.g. pressure sensor, thermistor, induction cell) from Device metadata table. Can be repeated for any number of sensors, with Roman numeral representing sensor number. |  | Categorical. Must reference one-to-one to a sensor type listed in Device metadata table.|
| [Sensor I measurement](fields/sensorIMeasurement.md) | Measurement taken by a sensor at this time and location. Units of measurement and other relevant metadata documented in Device metadata table. Can be repeated for any number of sensors, with Roman numeral representing sensor number. |  | Unit as specified in Device metadata table for this sensor|
