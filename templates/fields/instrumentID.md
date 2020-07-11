# instrumentID 

## Definition 
Unique instrument ID. Can be the instrument serial number or similar identification system used by the manufacturer.

## Format
alpha-numerical, e.g. “09A0178”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|Unique ID|http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/|NERC/Sensor Web Enablement Marine Profiles/Sensor ML |
|Tag local identifier/Tag ID|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000182/|Movebank |
|instrument_name|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L2|Tagbase |

## SensorML example
```xml
<sml:identification>  
	<sml:IdentifierList>  
		<sml:identifier>  
			<sml:Term definition="http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/">  
				<sml:label>Instrument ID</sml:label>  
				<sml:value>SN123456789</sml:value>  
			</sml:Term>  
		</sml:identifier>  
	</sml:IdentifierList>  
</sml:identification>
```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
