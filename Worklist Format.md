# Sample Types
When the LIMS prepares a worklist file for instrument software,
it needs to include the sample type with each sample. To facilitate
interoperability, this standard defines the exact terms of sample types.
Both the LIMS and the instrument software can map the standard term into
its internal representation.

The following sample types are supported:

| Sample Type   | Description                       | Also known as |
| ------------- | --------------------------------- |---------------|
| Test Sample   | The sample under analysis         | Unknown       |
| Blank with IS |                                   | Control Blank |
| Blank         | A blank without internal standard | Double Blank  |
| Standard      |                                   |               |
| Solvent       |                                   | Wash Blank    |
| Stability     |                                   |               |
| Control       |                                   |               |
| QC            |                                   |               |
| Other         |                                   |               |
