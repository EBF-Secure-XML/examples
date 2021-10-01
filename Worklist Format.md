# Sample Types
When the LIMS prepares a worklist file for instrument software,
it needs to include the sample type with each sample. To facilitate
interoperability, this standard defines the exact terms of sample types.
Both the LIMS and the instrument software can map the standard term into
its internal representation.

The following sample types are supported:

| Sample Type   | Description                                       | Also known as |
| ------------- | ------------------------------------------------- |---------------|
| Test Sample   | Sample under analysis                             | Unknown       |
| Blank with IS | Blank sample that includes an internal standard   | Control Blank |
| Blank         | Blank sample without internal standard            | Double Blank  |
| Standard      |                                                   |               |
| Solvent       |                                                   | Wash Blank    |
| Stability     |                                                   |               |
| Control       |                                                   |               |
| QC            |                                                   |               |
| Other         |                                                   |               |

# Units for Analytes
This format assumes that a given analyte always uses the same unit across samples within a batch.
