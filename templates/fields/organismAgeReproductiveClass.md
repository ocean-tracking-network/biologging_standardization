# Field Name
organism Age Reproductive Class

## Definition 
Age class of organism carrying instrument at the time the tag was attached as adult (adu), sub-adult (sub), juvenile (juv), newborn or recently born (new), or unknown (unk).

## Format
Categorical: adu, sub, juv, new, unk

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
