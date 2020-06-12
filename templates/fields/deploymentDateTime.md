# Field Name
deployment Date Time

## Definition 
Timestamp the instrument was deployed on the animal

## Standard
ISO-8601

## Format
Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, eg. “2020-03-29T 17:56:10.000Z”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|time_coverage_start|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L45|Tagbase|
|deploy on timestamp|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000081|Movebank|
|eventDate|https://dwc.tdwg.org/terms/#dwc:eventDate/|Darwin Core|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
