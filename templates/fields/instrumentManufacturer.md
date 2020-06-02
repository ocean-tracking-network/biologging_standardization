# Instrument Manufacturer

## Definition 
Manufacturer of the instrument (eg. Wildlife Computers, SMRU, Lotek, Little Leonardo, etc.)

## Format
string, eg. “Wildlife Computers”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
||||

## SensorML example
```xml
<sml:identifier>
    <sml:Term definition="http://urlToDefinitionOf/field">
        <sml:label>Instrument Manufacturer</sml:label>
        <sml:value>Wildlife Computers</sml:value>
    </sml:Term>
</sml:identifier>
```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "instrumentManufacturer", "http://urlToDefinitionOf/field", "Wildlife Computers"
```