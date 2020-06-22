# Instrument Serial Number

## Definition 
Serial number of instrument deployed (may or may not be different from InstrumentID).

## Format
 alpha-numerical, e.g. “09A0178”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|Serial Number|http://vocab.nerc.ac.uk/collection/W07/current/IDEN0005/|NERC/Sensor Web Enablement Marine Profiles/Sensor ML|
|serial_number|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L9|Tagbase|
|Tag serial no|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000189/|NERC/MVB|

## SensorML example
```xml
    <!-- ======================================= -->
    <!--               Identifiers               -->
    <!-- ======================================= -->
<sml:identification>  
	<sml:IdentifierList>  
		<sml:identifier>  
			<sml:Term definition="http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/">  
				<sml:label>Serial Number</sml:label>  
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
institutionId:tagDeployment:XYZ, "Serial Number", "http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/", "09A0178"
```
