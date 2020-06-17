# Field Name
Species

## Definition 
Binomial species name of organism carrying instrument

## Standard
ITIS

## Format
String of the format “Genus species”, genus capitalized, separated by one space, eg. “Mirounga angustirostris”


## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|animal taxon|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000016/|Movebank|
|genus|https://dwc.tdwg.org/terms/#dwc:genus|Darwin Core|
|specific Epithet|https://dwc.tdwg.org/terms/#dwc:specificEpithet|Darwin Core|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
