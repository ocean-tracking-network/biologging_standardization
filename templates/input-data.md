## Table S4. Input data template 

Data fields provided by the researcher upon submission of data to repository (i.e. column headers). Alongside the completed Device Metadata table and Deployment Metadata table (linked by DeploymentID), this completes the submission to the repository. (CLS = Collecte Localisation Satellites)

| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [DeploymentID](fields/deploymentID.md) | Unique identifier for single deployment of device. |  | |
| [Time](fields/time.md) | Timestamp of data point  | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”|
| [Latitude](fields/latitude.md) | Latitude of data point | ISO 6709:2008 | Decimal degrees north, -90.0000 to 90.0000|
| [Longitude](fields/longitude.md) | Longitude of data point | ISO 6709:2008 | Decimal degrees east, -180.0000 to 180.0000|
| [Argos LC](fields/argosLC.md) | Argos location class of position | CLS Argos  | Categorial (G,3,2,1,0,A,B,Z)|
| [Argos Filter method](fields/argosFilterMethod.md) | Filter method implemented by CLS/Argos to generate location | CLS Argos  | Categorial: Least squares or Kalman|
| [Argos Error Radius](fields/argosErrorRadius.md) | Error radius for location provided by CLS/Argos | CLS Argos  | meters|
| [Argos semi major](fields/argosSemiMajor.md) | Length of semi-major axis of error ellipse provided by CLS/Argos. Defaults to NA if Least-Squares Data | CLS Argos  | meters|
| [Argos semi minor](fields/argosSemiMinor.md) | Length of semi-minor axis of error ellipse provided by CLS/Argos. Defaults to NA if Least-Squares Data | CLS Argos  | meters|
| [Argos orientation](fields/argosOrientation.md) | Orientation of error ellipse provided by CLS/Argos | CLS Argos  | degrees from North (heading east)|
| [Argos GDOP](fields/argosGDOP.md) | Geometric Dilution of Precision provided by CLS/Argos | CLS Argos  | m/Hz|
| [GPS satellite count](fields/gpsSatelliteCount.md) |  |  | numerical eg. “4”|
| [Residuals (FastLoc)](fields/residualsFastLoc.md) |  |  | |
| [Temperature (GLS)](fields/temperatureGls.md) |  |  | numerical in °C|
| [Depth (GLS)](fields/depthGls.md) |  |  | |
| [Angle (GLS)?](fields/angleGls)?.md) |  |  | |
| [Sensor I type](fields/sensorIType.md) | Type of sensor contained in tag (eg. pressure sensor, thermistor, induction cell, etc) from Device metadata table. |  | Categorical. Must reference one-to-one to a sensor type listed in Device metadata table.|
| [Sensor I measurement](fields/sensorIMeasurement.md) | Measurement taken by a sensor at this time and location. Can be repeated for any number of sensors. Units of measurement and other relevant metadata documented in Device metadata table. |  | Unit as specified in Device metadata table for this sensor|