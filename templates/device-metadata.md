## Table S1: Device metadata template

Metadata describing instrument specifications and included sensors, such as those providing horizontal, vertical, environmental, physiological, and accelerometry data. The Device metadata template is to be completed by the instrument manufacturer and should be provided to the researcher using the device or, in cases where data uploading to a compliant repository is done directly by the manufacturer, should be uploaded with the data. All attributes are mandatory, but fields can be “unknown” or “NA” if data do not exist or are not applicable to a specific device. Sensor metadata can be repeated for any number of separate sensors on a device, with separate sensors assigned Roman numerals (Sensor I, Sensor II, Sensor III, etc.). 

ISO: International Organization for Standardization

| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [instrumentID](fields/instrumentID.md) | Unique instrument ID. Can be the instrument serial number, or other similar identification system used by the manufacturer. | | alpha-numerical, eg. “09A0178”|


### Instrument specifications
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [instrumentType](fields/instrumentType.md) | Type of instrument deployed (e.g. archival, satellite, rapid-acquisition, acoustic tag, acoustic receiver). | | categorical, e.g. “satellite”|	
| [instrumentModel](fields/instrumentModel.md) | Name of specific instrument model deployed. | | string, e.g. “Mk10”|  
| [instrumentManufacturer](fields/instrumentManufacturer.md) | Manufacturer of the instrument (e.g. Wildlife Computers, SMRU, Lotek, Little Leonardo). | | string, e.g. “Wildlife Computers”| 
| [instrumentSerialNumber](fields/instrumentSerialNumber.md) | Serial number of instrument deployed. | | alpha-numerical, e.g. “09A0178”|  

### Horizontal sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [trackingDevice](fields/trackingDevice.md) | Type of tracking technology used (e.g. Argos, fast-acquisition GPS, GLS, acoustic). || categorial, e.g. “Argos”|
| [uplinkInterval](fields/uplinkInterval.md) | Interval of time between two consecutive message dispatches. | | Numerical in seconds| 	

### Vertical sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [unitsReported](fields/unitsReported.md) | Unit of altidue/depth reported. | | string, e.g. “meters”|	
| [resolution](fields/resolution.md) | Resolution of altitude/depth measurements in same unit specified for vertical sensor. | |numerical, e.g. “0.1”	
| [lowerSensorDetectionLimit](fields/lowerSensorDetectionLimit.md) | Lower detection limit for sensor in same unit specified for sensor. | |numerical e.g. “5”| 
| [upperSensorDetectionLimit](fields/upperSensorDetectionLimit.md) | Upper detection limit for sensor in same unit specified for sensor. | | numerical e.g. “2500”| 
| [sensorPrecision](fields/sensorPrecision.md) | Sensor precision in same unit specified for sensor. | | numerical e.g. “+/- 0.01”| 
| [sensorSamplingFrequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement. | | Numercial in Hz| 
| [sensorDutyCycling](fields/sensorDutyCycling.md) | Description of any duty cycling assigned to sensor. | | string, eg. "records data only on deepest dive in 6 hr period"| 
| [sensorCalibrationDate](fields/sensorCalibrationDate.md) | Date when sensor calibration was done. | ISO-8601| Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”|
| [sensorCalibrationDetails](fields/sensorCalibrationDetails.md) | Full definition of the calibration done through addition of a link to where the data and/or methods are described (e.g. peer-reviewed publication). | | DOI or URL| 

### Environmental sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [sensorType](fields/sensorType.md) | Type of sensor contained in instrument (e.g. thermistor, induction cell, conductivity cell, fluorometer, optode). | | categorical, e.g. “fluorometer”|	
| [sensorManufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor (may or may not be the same as the instrument manufacturer). | | string, e.g. “Valeport”|  
| [sensorModel](fields/sensorModel.md) | Name of specific sensor model. | | string, e.g. “Cyclops 7”|  
| [unitsReported](fields/unitsReported.md) | Unit of oceanographic variable reported. | | string, e.g. “degrees C”|  
| [lowerSensorDetectionLimit](fields/lowerSensorDetectionLimit.md) | Lower detection limit for sensor in same unit specified for sensor. | | numerical e.g. “-2”|  
| [upperSensorDetectionLimit](fields/upperSensorDetectionLimit.md) | Upper detection limits for sensor in same unit specified for sensor. | | numerical e.g. “35”|  
| [sensorPrecision](fields/sensorPrecision.md) | Sensor precision in same unit specified for sensor. | | numerical e.g. “+/- 0.01”|  
| [sensorSamplingFrequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement. | | Numercial in Hz|  
| [sensorDutyCycling](fields/sensorDutyCycling.md) | Description of any duty cycling assigned to sensor. |  | string, eg. "records data only on deepest dive in 6 hr period"|  
| [sensorCalibrationDate](fields/sensorCalibrationDate.md) | Date when sensor calibration was done. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”| 	
| [sensorCalibrationDetails](fields/sensorCalibrationDetails.md) | Full definition of the calibration done through addition of a link to where the data and/or methods are described (e.g. peer-reviewed publication). | | DOI or URL|  

### Physiological sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [sensorType](fields/sensorType.md) | Type of sensor in instrument (e.g. heart oxygen probe, blood oxygen probe). || string, e.g. “heart rate monitor”| 
| [sensorManufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor (may or may not be the same as the instrument manufacturer). | | string |  
| [sensorModel](fields/sensorModel.md) | Name of specific sensor model. | | string |  
| [sensorUnits](fields/sensorUnits.md) | Unit of physiological variable reported. | |categorical|  
| [lowerSensorDetectionLimit](fields/lowerSensorDetectionLimit.md) | Lower detection limit for sensor in same unit specified for sensor. | | numerical|  
| [upperSensorDetectionLimit](fields/upperSensorDetectionLimit.md) | Upper detection limit for sensor in same unit specified for sensor. | | numerical|  
| [sensorPrecision](fields/sensorPrecision.md) | Sensor precision in same unit specified for sensor. | | numerical|  
| [sensorSamplingFrequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement. | | Numercial in Hz| 	
| [sensorDutyCycling](fields/sensorDutyCycling.md) | Description of any duty cycling assigned to sensor. | | string, eg. "records data only on deepest dive in 6 hr period"|  
| [sensorCalibrationDate](fields/sensorCalibrationDate.md) | Date when sensor calibration was done. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”| 
| [sensorCalibrationDetails](fields/sensorCalibrationDetails.md) | Full definition of the calibration done through addition of a link to where the data and/or methods are described (e.g., peer-reviewed publication). | | DOI or URL | 	

### Accelerometry sensors
| attributeName | description | standard | format | 
| ------------- | ----------- | -------- | -------- |
| [sensorManufacturer](fields/sensorManufacturer.md) | Name of the manufacturer of the sensor (may or may not be the same as the instrument manufacturer). | | string, e.g. “Little Leonardo”| 	
| [sensorModel](fields/sensorModel.md) | Name of specific sensor model. | |string|  
| [axes](fields/axes.md) | Axes in which acceleration is logged. | |Categorical (combinations of x, y, and z)| 
| [sensorUnits](fields/sensorUnits.md) | Unit of physiological variable reported. | |categorical|  
| [lowerSensorDetectionLimit](fields/lowerSensorDetectionLimit.md) | Lower detection limit for sensor in same unit specified for sensor. | |numerical|  
| [upperSensorDetectionLimit](fields/upperSensorDetectionLimit.md) | Upper detection limit for sensor in same unit specified for sensor. | |numerical|  
| [sensorPrecision](fields/sensorPrecision.md) | Sensor precision in same unit specified for sensor. | |numerical|  
| [sensorSamplingFrequency](fields/sensorSamplingFrequency.md) | How often the sensor records a measurement. | |Numercial in Hz|  
| [sensorDutyCycling](fields/sensorDutyCycling.md) | Description of any duty cycling assigned to sensor. | | string, eg. "records data only on deepest dive in 6 hr period"|  
| [sensorCalibrationDate](fields/sensorCalibrationDate.md) | Date when sensor calibration was done. | ISO-8601 | Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”| 
| [sensorCalibrationDetails](fields/sensorCalibrationDetails.md) | Full definition of the calibration done through addition of a link to where the data and/or methods are described (e.g., peer-reviewed publication). | | DOI or URL| 	


