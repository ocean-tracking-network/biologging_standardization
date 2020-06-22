# Sensor I Type

## Definition 
Type of sensor contained in tag (e.g. pressure sensor, thermistor, induction cell, etc) from Device metadata table. Can be repeated for any number of sensors, with Roman numeral representing sensor number.

## Format
Categorical. Must reference one-to-one to a sensor type listed in Device metadata table.

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|sensor type|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000170/|Movebank|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
