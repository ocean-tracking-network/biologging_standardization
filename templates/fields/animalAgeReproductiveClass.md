# Field Name
animal Age Reproductive Class

## Definition 
Age class of animal carrying instrument at the time the tag was attached

## Format
Categorical: ad, juv, unk

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|animal life stage|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000018/|Movebank|
|lifestage_capture|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L76|Tagbase|
|lifestage_recapture|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L77|Tagbase|
|lifeStage|https://dwc.tdwg.org/terms/#dwc:lifeStage|Darwin Core|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
