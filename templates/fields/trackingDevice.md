# Tracking device

## Definition 
 Type of tracking technology used (eg. Argos, FastLoc, GLS, acoustic, etc) 

## Format
 categorial, eg. “Argos”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|Sensor type|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000170/|NERC/MVB|
|waypoints_source (?)|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L124|Tagbase|

## SensorML example
```xml
<sml:classifier>
    <sml:Term definition="http://vocab.nerc.ac.uk/collection/MVB/current/MVB000170/">
        <sml:label>Tracking device</sml:label>
        <sml:codeSpace xlink:href="urn:x-ceos:def:GCMD:sensors"/>
        <sml:value>gamma detector</sml:value>
    </sml:Term>
</sml:classifier>
```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "Tracking device", "http://vocab.nerc.ac.uk/collection/MVB/current/MVB000170/", "gamma detector"
```