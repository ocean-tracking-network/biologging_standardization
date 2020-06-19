# Field Name
Deployment latitude

## Definition 
Latitude in decimal degrees of tag deployment.

## Standard
ISO 6709:2008

## Format
Decimal degrees north, -90.0000 to 90.0000

## Similar Terms 
|Term|Definition URL|Source Vocabulary Publisher/Creator|
|----|----------|-----------------|
|geospatial_lat_start|https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L42|Tagbase|
|deploy on latitude|http://vocab.nerc.ac.uk/collection/MVB/current/MVB000078/|Movebank|
|decimal_Latitude|http://rs.tdwg.org/dwc/terms/decimalLatitude|Darwin Core|

## SensorML example
```xml

```
## Darwin Core example
```csv
# measurementOrFact.csv
eventId, measurementType, measurementTypeID, measurementValue
institutionId:tagDeployment:XYZ, "fieldName", "http://urlToDefinitionOf/field", "value"
```
