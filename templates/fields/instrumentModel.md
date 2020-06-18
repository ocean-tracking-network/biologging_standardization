# Instrument Model

## Definition 
Name of specific tag model deployed.

## Format
string, e.g. “Mk10”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|Tag Model|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000185/|Movebank|
|Model|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L6|Tagbase|
|Model Name|http://vocab.nerc.ac.uk/collection/W07/current/IDEN0003/|NERC/Sensor Web Enablement Marine Profiles|
|Model Number|http://vocab.nerc.ac.uk/collection/W07/current/IDEN0004/|NERC/Sensor Web Enablement Marine Profiles|

## SensorML example
```xml
<sml:identification>
        <sml:IdentifierList>
            <sml:identifier>
                <sml:Term definition="http://urlToDefinitionOf/instrumentModel">
                    <sml:label>Instrument Model</sml:label>
                    <sml:value>Mk10</sml:value>
                </sml:Term>
            </sml:identifier>
       </sml:IdentifierList>
 </sml:identification>"
  ```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "instrumentModel", "http://urlToDefinitionOf/InstrumentModel", "Mk10"
