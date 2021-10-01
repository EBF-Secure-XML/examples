# Result Format Description

## Sample Identification
In the worklist, each sample can carry up to three identifiers:
* `sampleId` (mandatory, unique)
* `barcode` (optional)
* `name` (mandatory, may be blank)
* `locationInContainer` (mandatory)
* `containerID` (mandatory if multiple containers/plates are used)

When reporting results, it is expected that all identifiers supplied 
via the worklist are returned. These identifiers allow the leading 
system to map the results to its experiment definitions.

### Example
```xml
<Sample sampleID="Cypro-2016_001 CAL01"
        barcode="5699_0"
        name="4 1 Cypro-2016_001 CAL01 1 1" 
        locationInContainer="A1" 
        containerID="plate0" >...</Sample>
```

## Sample Parameters
The sample parameters submitted in the worklist document only need
to be reported back in the result document if they deviated from the
original in the worklist document (e.g., were
changed in the instrument software manually). Otherwise, the leading
system can assume that the sequence was performed as instructed in the
worklist document.

Reporting all parameters is useful for documentation purposes -- it
allows tracking what was actually done. 

### Example
```xml
<Sample sampleID="4 1 Cypro-2016_001 CAL01 1 1" barcode="Lab A 12C 124_5699_0" name="4 1 Cypro-2016_001 CAL01 1 1" locationInContainer="A1" containerID="plate0">
   <Category name="Sample Info">
    <Parameter name="Sample Type" parameterType="String">
      <S>STANDARD</S>
    </Parameter>
    <Parameter name="Dilution Factor" parameterType="Float32">
      <F>1.0</F>
    </Parameter>
  </Category>
  <Category name="Analytes">
    <Category name="Analyte">
      <Parameter name="Substance" parameterType="String">
        <S>cyprofloxacin</S>
      </Parameter>
      <Parameter name="Concentration" parameterType="Float32">
        <F>1.1</F>
        <Unit label="pg/mL"/>
      </Parameter>
    </Category>
  </Category>
</Sample>
```