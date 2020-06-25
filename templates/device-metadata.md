## Table S1: Device metadata template



| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [InstrumentID](fields/instrumentID.md) | Unique instrument ID. Can be the instrument serial number, or other similar identification system used by the manufacturer. | | alpha-numerical, eg. “09A0178”|


### Instrument specifications
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [Instrument type](fields/instrumentType.md) | Type of instrument deployed (e.g. archival, satellite, rapid-acquisition, acoustic tag, acoustic receiver). | | categorical, e.g. “satellite”|
| [Instrument model](fields/instrumentModel.md) | Name of specific instrument model deployed. | | string, e.g. “Mk10”|
| [Instrument Manufacturer](fields/instrumentManufacturer.md) | Manufacturer of the instrument (e.g. Wildlife Computers, SMRU, Lotek, Little Leonardo). | | string, e.g. “Wildlife Computers”|
| [Instrument Serial Number](fields/instrumentSerialNumber.md) | Serial number of instrument deployed. | | alpha-numerical, e.g. “09A0178”|

### Horizontal sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [Tracking device](fields/trackingDevice.md) | Type of tracking technology used (e.g. Argos, fast-acquisition GPS, GLS, acoustic). || categorial, e.g. “Argos”|
| [Repetition rate](fields/repetitionRate.md) | Interval of time between two consecutive message dispatche.s | | Seconds|

### Vertical sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [Units reported](fields/unitsReported.md) | Unit of altidue/depth reported. | CF | string, e.g. “meters”|
| [Resolution](fields/resolution.md) | Resolution of altitude/depth measurements in same unit specified for vertical sensor. | |numerical, e.g. “0.1”
| [Lower sensor detection limit](fields/lowerSensorDetectionLimit.md) | Lower detection limit for sensor in same unit specified for sensor. | |numerical e.g. “5”|
| [Upper sensor detection limit](fields/upperSensorDetectionLimit.md) | Upper detection limit for sensor in same unit specified for sensor. | | numerical e.g. “2500”|
| [Sensor precision](fields/sensorPrecision.md) | Sensor precision in same unit specified for sensor. | | numerical e.g. “+/- 0.01”|
| [Sensor sampling frequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement. | | e.g. “1 Hz”|
| [Sensor duty cycling](fields/sensorDutyCycling.md) | Description of any duty cycling assigned to sensor. | | string|
| [Sensor calibration date](fields/sensorCalibrationDate.md) | Date when sensor calibration was done. | ISO-8601| Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”|
| [Sensor calibration details](fields/sensorCalibrationDetails.md) | Full definition of the calibration done through addition of a link to where the data and/or methods are described (e.g. peer-reviewed publication). | | DOI or URL|

### Environmental sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [Sensor type](fields/sensorType.md) | Type of sensor contained in instrument (e.g. thermistor, induction cell, conductivity cell, fluorometer, optode). | | categorical, e.g. “fluorometer”|
| [Sensor manufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor (may or may not be the same as the instrument manufacturer). | | string, e.g. “Valeport”|
| [Sensor model](fields/sensorModel.md) | Name of specific sensor model. | | string, e.g. “Cyclops 7”|
| [Units reported](fields/unitsReported.md) | Unit of oceanographic variable reported. | | string, e.g. “degrees C”|
| [Lower sensor detection limit](fields/lowerSensorDetectionLimit.md) | Lower detection limit for sensor in same unit specified for sensor. | | numerical e.g. “-2”|
| [Upper sensor detection limit](fields/upperSensorDetectionLimit.md) | Upper detection limits for sensor in same unit specified for sensor. | | numerical e.g. “35”|
| [Sensor precision](fields/sensorPrecision.md) | Sensor precision in same unit specified for sensor. | | numerical e.g. “+/- 0.01”|
| [Sensor sampling frequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement. | | e.g. “1 Hz”|
| [Sensor duty cycling](fields/sensorDutyCycling.md) | Description of any duty cycling assigned to sensor. |  | string|
| [Sensor calibration date](fields/sensorCalibrationDate.md) | Date when sensor calibration was done. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”|
| [Sensor calibration details](fields/sensorCalibrationDetails.md) | Full definition of the calibration done through addition of a link to where the data and/or methods are described (e.g. peer-reviewed publication). | | DOI or URL|
### Physiological sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [Sensor Type](fields/sensorType.md) | Type of sensor in instrument (e.g. heart oxygen probe, blood oxygen probe). || string, e.g. “heart rate monitor”|
| [Sensor Manufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor (may or may not be the same as the instrument manufacturer). | | string |
| [Sensor Model](fields/sensorModel.md) | Name of specific sensor model. | | string |
| [Sensor units](fields/sensorUnits.md) | Unit of physiological variable reported. | |categorical|
| [Lower sensor detection limit](fields/lowerSensorDetectionLimit.md) | Lower detection limit for sensor in same unit specified for sensor. | | numerical|
| [Upper sensor detection limit](fields/upperSensorDetectionLimit.md) | Upper detection limit for sensor in same unit specified for sensor. | | numerical|
| [Sensor precision](fields/sensorPrecision.md) | Sensor precision in same unit specified for sensor. | | numerical|
| [Sensor sampling frequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement. | | numerical, e.g. “4 Hz”|
| [Sensor duty cycling](fields/sensorDutyCycling.md) | Description of any duty cycling assigned to sensor. | | string|
| [Sensor calibration date](fields/sensorCalibrationDate.md) | Date when sensor calibration was done. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”|
| [Sensor calibration details](fields/sensorCalibrationDetails.md) | Full definition of the calibration done through addition of a link to where the data and/or methods are described (e.g., peer-reviewed publication). | | DOI or URL |
### Accelerometry sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [Sensor Manufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor (may or may not be the same as the instrument manufacturer). | | string, e.g. “Little Leonardo”|
| [Sensor Model](fields/sensorModel.md) | Name of specific sensor model. | |string|
| [Axes](fields/axes.md) | Axes in which acceleration is logged. | |Categorical (combinations of x, y, and z)|
| [Sensor units](fields/sensorUnits.md) | Unit of physiological variable reported. | |categorical|
| [Lower sensor detection limit](fields/lowerSensorDetectionLimit.md) | Lower detection limit for sensor in same unit specified for sensor. | |numerical|
| [Upper sensor detection limit](fields/upperSensorDetectionLimit.md) | Upper detection limit for sensor in same unit specified for sensor. | |numerical|
| [Sensor precision](fields/sensorPrecision.md) | Sensor precision in same unit specified for sensor. | |numerical|
| [Sensor sampling frequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement. | |numerical|
| [Sensor duty cycling](fields/sensorDutyCycling.md) | Description of any duty cycling assigned to sensor. | | string|
| [Sensor calibration date](fields/sensorCalibrationDate.md) | Date when sensor calibration was done. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”|
| [Sensor calibration details](fields/sensorCalibrationDetails.md) | Full definition of the calibration done through addition of a link to where the data and/or methods are described (e.g., peer-reviewed publication). | | DOI or URL|
