# Field Name
Detachment date and  time

## Definition 
Timestamp of when the instrument was recovered or otherwise detached from the organism.

## Standard
ISO-8601

## Format
Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|deploy off timestamp|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000077/|Movebank|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
