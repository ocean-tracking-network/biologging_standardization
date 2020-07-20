Example - Export to Darwin Core format
================

This demonstrates exporting the example Level 3 output dataset to the
Darwin Core Archive format for packaging and publication to biodiversity
repositories (eg. GBIF, OBIS, Living Atlases). The format is described
in the Darwin Core [text guide](https://dwc.tdwg.org/text/). This
example uses the OBIS ENV-DATA approach, described
[here](https://obis.org/manual/dataformat/).

## Data In

The data used here are associated with Braun CD, Gaube P,
Sinclair-Taylor TH, Skomal GB, Thorrold SR (2019) Mesoscale eddies
release pelagic sharks from thermal constraints to foraging in the ocean
twilight zone. Proc Natl Acad Sci U S A 116:17187–17192 (doi:
[10.1073/pnas.1903067116](https://doi.org/10.1073/pnas.1903067116)), and
the data are archived at DataOne (doi:
[10.24431/rw1k329](https://doi.org/10.24431/rw1k329)).

Reading the data from the files which are formatted to the metadata
templates:

``` r
deployment_metadata <- read.csv("../braun_blues_deployment-metadata.csv")
device_metadata <- read.csv("../braun_blues_device-metadata.csv")
obs_data <- read.csv("../data_level3/blue_sharks_level3.csv")
```

## Darwin Core entities

The data is spread across a number of files which are zipped into the
archive:

  - **event.csv** the Event Core outlines major project milesones such
    as capture, deployment, and the deployment completion
  - **occurrence.csv** the Occurrence Extension contains each occurrence
    record, usually a HumanObservation which is associated with the
    initial capture and biota measurements, then a series of
    MachineObservations associated with the tag and sensor information.
  - **extendedMeasurementOrFact.csv** the Extended Measurement or Fact
    Extension contains any measurement or information related to any
    Event or Occurrence, eg. sensor metadata
  - **meta.xml** provides a machine readable document describing the
    structure of the archive
  - **eml.xml** contains standard scientific publication metadata
    expressed in Ecological Modelling Language

### Event Core

3 key events in this dataset can be mapped from the
**deployment-metadata**:

  - Deployment Start / capture
  - Tag Deployment
  - Deployment End

These event records are linked to from occurrence and measurement
records.

    ##                    eventID organismID     eventRemarks
    ## 1 160424_2016_106744:start         NA Deployment Start
    ## 2       160424_2016_106744         NA       Deployment
    ## 3   160424_2016_106744:end         NA   Deployment End
    ##                                           eventDate decimalLatitude
    ## 1                          2016-08-27T 00:00:00.00Z        41.40433
    ## 2 2016-08-27T 00:00:00.00Z/2017-02-15T 00:00:00.00Z              NA
    ## 3                          2017-02-15T 00:00:00.00Z        35.08900
    ##   decimalLongitude
    ## 1        -69.29867
    ## 2               NA
    ## 3        -73.91500

### Occurrence Extension

Biodiversity infrastructures index by occurrence records, denoting
species-location-time, and manage them by a semi-controlled vocabulary
in the [basisOfRecord
term](https://dwc.tdwg.org/terms/#dwc:basisOfRecord) which delineates
HumanObservations, MachineObservations, PreservedSpecimen etc.

The archive will record a HumanObservation record which aligns with the
animal capture/deployment start event, and will link to observed biotic
measurements. MachineObservation occurrence records are features
recorded by the tag with spatial and temporal components.

    ##                    eventID             occurrenceID                eventDate
    ## 1 160424_2016_106744:start 160424_2016_106744:start 2016-08-27T 00:00:00.00Z
    ## 2       160424_2016_106744  160424_2016_106744:1303      2016-08-27 23:00:00
    ## 3       160424_2016_106744  160424_2016_106744:1304      2016-08-28 23:00:00
    ##        basisOfRecord organismID decimalLatitude decimalLongitude
    ## 1   HumanObservation         NA        41.40433        -69.29867
    ## 2 MachineObservation         NA        41.41600        -69.15700
    ## 3 MachineObservation         NA        41.40500        -69.06418
    ##    scientificName vernacularName                          scientificNameID  sex
    ## 1 Prionace glauca     blue shark urn:lsid:marinespecies.org:taxname:105801    M
    ## 2 Prionace glauca           <NA>                                      <NA> <NA>
    ## 3 Prionace glauca           <NA>                                      <NA> <NA>
    ##   reproductiveCondition
    ## 1                   adu
    ## 2                  <NA>
    ## 3                  <NA>

### Measurement or Fact Extension

This extension contains measurements and data that are not defined in
the DarwinCore terms, have different cardinality to the occurrence or
event records (ie many acceleromter records) and usually without a
spatial component.

In this example this includes all of the tag/device metadata, some of
the animal measurements, and the detachment information. Each term
should have a definition URI.

    ##                    eventID             occurrenceID        measurementType
    ## 1 160424_2016_106744:start 160424_2016_106744:start  trappingMethodDetails
    ## 2 160424_2016_106744:start 160424_2016_106744:start       attachmentMethod
    ## 3       160424_2016_106744                                    instrumentID
    ## 4       160424_2016_106744                                             PTT
    ## 5       160424_2016_106744                                 instrumentModel
    ## 6       160424_2016_106744                          instrumentManufacturer
    ##                                                              measurementTypeID
    ## 1                                                                             
    ## 2 https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L26
    ## 3                     http://vocab.nerc.ac.uk/collection/W07/current/IDEN0008/
    ## 4 https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L12
    ## 5  https://github.com/tagbase/tagbase/blob/master/eTagMetadataInventory.csv#L6
    ## 6                     http://vocab.nerc.ac.uk/collection/W07/current/IDEN0012/
    ##     measurementValue
    ## 1       rod and reel
    ## 2         dorsal fin
    ## 3            15U2175
    ## 4             106744
    ## 5           SPOT258G
    ## 6 Wildlife Computers

## Final packaging

Each file is packaged into a zip with metadata files meta.xml and
eml.xml.

``` r
write.csv(eventdf,"event.csv",row.names = FALSE)
write.csv(occurrencesdf,"occurrence.csv",row.names = FALSE)
write.csv(mofdf,"mof.csv",row.names = FALSE)
zip("braun-blueshark-dwca.zip",files=c("event.csv","occurrence.csv","mof.csv","eml.xml","meta.xml"))
```
