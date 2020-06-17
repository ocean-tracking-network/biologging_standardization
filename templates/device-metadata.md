## Table S1: Device metadata template


| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | ------ |
| [InstrumentID](fields/instrumentID.md) | Serial number of tag, unless manufacturer uses alternative system | alpha-numerical, eg. “09A0178”|


### Instrument specifications
| attributeName | description | format | 
| ------------- | ----------- | ------ |
| [Instrument type](fields/instrumentType.md) | Type of tag deployed (eg. archival, satellite, popup, acoustic tag, acoustic receiver) | categorical, eg. “satellite”|
| [Instrument model](fields/instrumentModel.md) | Name of specific tag model deployed | string, eg. “Mk10”|
| [Instrument Manufacturer](fields/instrumentManufacturer.md) | Manufacturer of the instrument (eg. Wildlife Computers, SMRU, Lotek, Little Leonardo, etc.) | string, eg. “Wildlife Computers”|
| [Instrument Serial Number](fields/instrumentSerialNumber.md) | Serial number of tag deployed | alpha-numerical, eg. “09A0178”|

### Horizontal sensors
| attributeName | description | format | 
| ------------- | ----------- | ------ |
| [Tracking device](fields/trackingDevice.md) | Type of tracking technology used (eg. Argos, FastLoc, GLS, acoustic, etc) | categorial, eg. “Argos”|
| [Repetition rate](fields/repetitionRate.md) | Interval of time between two consecutive message dispatches | Seconds|

### Vertical sensors
| attributeName | description | format | 
| ------------- | ----------- | ------ |
| [Unit of altitude/depth ](fields/unitOfAltitudeDepth.md) | Unit of depth reported | categorical eg. “meters”|
| [Accuracy](fields/accuracy.md) | Accuracy of depth measurements in same unit specified for depth sensor | numerical, eg. “0.1”|
| [Resolution](fields/resolution.md) | Resolution of depth measurements in same unit specified for depth sensor | numerical, eg. “0.1”|
| [Pressure sampling frequency](fields/pressureSamplingFrequency.md) | Sampling frequency of depth measurements | eg. “0.25 Hz”|
| [Sensor detection limits](fields/sensorDetectionLimits.md) | Maximum detection limits of depth sensor in same unit specified for depth sensor | numerical. eg. “2500”|
### Environmental sensors
| attributeName | description | format | 
| ------------- | ----------- | ------ |
| [Sensor type](fields/sensorType.md) | Type of sensor contained in tag (eg. thermistor, induction cell, conductivity cell, fluorometer, optode, etc) | categorical, eg. “fluorometer”|
| [Sensor manufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor | string, eg. “Valeport”|
| [Sensor model](fields/sensorModel.md) | Name of specific sensor model | string, eg. “Cyclops 7”|
| [Units reported](fields/unitsReported.md) | Unit of oceanographic variable reported | string, eg. “degrees C”|
| [Lower sensor detection limit](fields/lowerSensorDetectionLimit.md) | Bottom detection limits for sensor in same unit specified for sensor | numerical eg. “-2”|
| [Upper sensor detection limits](fields/upperSensorDetectionLimit.md) | Upper detection limits for sensor in same unit specified for sensor | numerical eg. “35”|
| [Sensor accuracy/precision](fields/sensorAccuracyPrecision.md) | Sensor accuracy in same unit specified for sensor | numerical eg. “+/- 0.01”|
| [Sensor sampling frequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement (and duty cycling if applicable) | eg. “1 Hz”|
| [Date Calibrated](fields/dateCalibrated.md) | Date calibrations done | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”|
| [Calibration details](fields/calibrationDetails.md) | link to data and/or methods when possible | DOI or URL|
### Physiological sensors
| attributeName | description | format | 
| ------------- | ----------- | ------ |
| [Sensor Type](fields/sensorType.md) | Type of sensor in tag | string, eg. “heart rate monitor”|
| [Sensor Manufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor | string|
| [Sensor Model](fields/sensorModel.md) | Name of specific sensor model | string|
| [Sensor units](fields/sensorUnits.md) | Unit of physiological variable reported | categorical|
| [Lower sensor detection limit](fields/lowerSensorDetectionLimit.md) | Bottom detection limits for sensor in same unit specified for sensor | numerical|
| [Upper sensor detection limit](fields/upperSensorDetectionLimit.md) | Upper detection limits for sensor in same unit specified for sensor | numerical|
| [Sensor precision/accuracy](fields/sensorPrecisionAccuracy.md) | Sensor accuracy in same unit specified for sensor | numerical|
| [Sampling frequency](fields/samplingFrequency.md) | How often the sensor records a measurement (and duty cycling if applicable) | numerical, eg. “4 Hz”|
| [Sensor calibrations](fields/sensorCalibrations.md) | Type of calibrations done with link to data when possible | String (possibly a reference to data)|
### Accelerometry sensors
| attributeName | description | format | 
| ------------- | ----------- | ------ |
| [Sensor Manufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor | string, eg. “Little Leonardo”|
| [Sensor Model](fields/sensorModel.md) | Name of specific sensor model | string|
| [Axes](fields/axes.md) | Axes in which acceleration is logged | Categorical (combinations of x, y, and z)|
| [Sampling frequency](fields/samplingFrequency.md) | How often the sensor records a measurement (and duty cycling if applicable) | Numerical|
| [Calibrations, if applicable](fields/calibrations.md) | Calibrations performed on physiological sensor | String (possible link to data via DOI or URL)|