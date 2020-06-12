# Field Name
track Start Time

## Definition 
Timestamp at which animal track starts if different from deployment time (to, for example, cut out instrument tests done before deployment)

## Standard
ISO-8601

## Format
Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|timestamp of first deployed location|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000240/|Movebank|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
