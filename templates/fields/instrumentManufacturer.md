# Instrument Manufacturer

## Definition 
Manufacturer of the instrument (eg. Wildlife Computers, SMRU, Lotek, Little Leonardo, etc.)

## Format
string, eg. “Wildlife Computers”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|Manufacturer|http://vocab.nerc.ac.uk/collection/W07/current/IDEN0012/|NERC/Sensor Web Enablement Marine Profiles/Sensor ML|
|Tag Manufacturer Name|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000183/|NERC/MVB|
|manufacturer|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L5|Tagbase|

## SensorML example
```xml
<sml:identifier>
    <sml:Term definition="http://vocab.nerc.ac.uk/collection/W07/current/IDEN0012/">
        <sml:label>Manufacturer</sml:label>
        <sml:value>Wildlife Computers</sml:value>
    </sml:Term>
</sml:identifier>
```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "Manufacturer", "http://vocab.nerc.ac.uk/collection/W07/current/IDEN0012/", "Wildlife Computers"
```