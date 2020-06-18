# Tracking device

## Definition 
Type of tracking technology used (eg. Argos, rapid aqcuisition GPS, GLS, acoustic). 

## Format
 categorial, e.g. “Argos”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|Sensor type|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000170/|NERC/MVB|
|waypoints_source (?)|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L124|Tagbase|

## SensorML example
```xml
<sml:classifier>
    <sml:Term definition="http://vocab.nerc.ac.uk/collection/MVB/current/MVB000170/">
        <sml:label>sensor type</sml:label>
        <sml:codeSpace xlink:href="urn:x-ceos:def:GCMD:sensors"/>
        <sml:value>Argos Doppler shift</sml:value>
    </sml:Term>
</sml:classifier>
```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "Tracking device", "http://vocab.nerc.ac.uk/collection/MVB/current/MVB000170/", "gamma detector"
```
