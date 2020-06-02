# Tracking device

## Definition 
 Type of tracking technology used (eg. Argos, FastLoc, GLS, acoustic, etc) 

## Format
 categorial, eg. “Argos”

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
||||

## SensorML example
```xml
<sml:classifier>
    <sml:Term definition="http://sensorml.com/ont/swe/property/TrackingType">
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
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```