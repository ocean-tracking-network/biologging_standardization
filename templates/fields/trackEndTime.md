# Field Name
Track end time

## Definition 
Timestamp at which track of animal ends (may or may not be different from detachment data and time).

## Standard
ISO-8601

## Format
Datetime in UTC, yyyy-MM-ddT HH:mm:ss.SSSZ, e.g. “2020-03-29T 17:56:10.000Z”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|time_coverage_end|https://github.com/tagbase/tagbase/blob/master/eTag|Tagbase|
|timestamp of last deployed location|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000241/|Movebank|
|eventDate|https://dwc.tdwg.org/terms/#dwc:eventDate|DarwinCore|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
