# Instrument Serial Number

## Definition 
Serial number of tag deployed 

## Format
 alpha-numerical, eg. “09A0178”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
||||

## SensorML example
```xml
    <!-- ======================================= -->
    <!--               Identifiers               -->
    <!-- ======================================= -->
<sml:identification>
    <sml:IdentifierList>
		<sml:identifier>
            <sml:Term definition="http://sensorml.com/ont/swe/property/SerialNumber">
                <sml:label>Instrument Serial Number</sml:label>
                <sml:value>09A0178</sml:value>
            </sml:Term>
		</sml:identifier>
	</sml:IdentifierList>
</sml:identification>
```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "Instrument Serial Number", "http://urlToDefinitionOf/InstrumentSerialNumber", "09A0178"
```