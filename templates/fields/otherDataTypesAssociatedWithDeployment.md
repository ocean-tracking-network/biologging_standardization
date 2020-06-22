# Field Name
Other data types associated with deployment

## Definition 
Additional data collected with instrument deployment, e.g. from ancillary sensors, photo-ID, biopsy sample for genetics.

## Format
string, e.g. “light level”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|associatedOccurances|http://rs.tdwg.org/dwc/terms/version/associatedOccurrences-2014-10-23|Darwin Core|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
