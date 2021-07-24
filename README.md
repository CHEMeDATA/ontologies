## CHEMeDATA six key formal concepts

CHEMeDATA proposes to define six key formal concepts (objects) for the annotation of chemistry data.

 - 1 [***Compound***](./compound)  
 - 2 [***Sample***](./sample) include ***Compound***s
 - 3 [***Reaction***](./reaction) formalize the transformation of reactants  ***Compound***(s) into products ***Compound***(s)
 - 4 [***Operation***](./operation/synthsis) transforms a ***Sample*** into another ***Sample***. Synthesis, extraction, purification, etc. are ***Operation***s.
 - 5 [***Analysis***](./analysis/NMR) provides information about a ***Sample***
 - 6 [***Assignment***](./assignment) combines one (or a set of) ***Analysis*** with one (or more) ***Compound***(s) 

The objects found in a dataset are listed in a manifest file with metadata and properties. A selection of objects and key metadata and properties can be registered with the DOI of the data set using the datacite "subject" field to make them "Findable".
  
### Basic objects
  * 1 ***Compound*** [![Compound](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/compound.json)](./compound)  
    * 2D [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/compound2D.json)](./compound)  
    * 3D [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/compound3D.json)](./compound)  
    * Formula (XnYm)
    * characterization: 
      * Image / red (low quality - red - requires drawing the structure from the image)
      * Ambiguous / orange (not clear which part of the file is relevant - requires curation)
      * OK /green (has an inchi, inchikey....)
  * 2 ***Sample*** [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/sample.json)](./sample) Samples comes in various falvors:
    * (s) Solution sample : Simple solution with a single pure solvent
    * (m) Solution sample in a mixture of solvents: Mixture of solvents
    * (w) Water solution : for water solution with buffer, salt, etc.
    * (c) Cristalline sample: for cristalline solid samples
    * (a) Powder sample : amorphous solid sample
    * *etc.*
    * characterization: 
      * No description / red
      * OK / green
### Complex objects (have parts that are basic or complex objects)
  * 3 ***Reaction*** 
  [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/reaction2.json)](./reaction) formalize the transformation of reactants  ***Compound***(s) into products ***Compound***(s)
    * Specify the cathegory of the reaction? [![Oxidation](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/reaction2Ox.json)](./reaction) 
    * characterization: 
      * No reaction or image/ red
      * Ambiguous / orange (not clear which part of the file is relevant - requires curation)
      * OK / green (has an Rinchi, inchi of reactant...)
  * 4 ***Operation*** transforms a ***Sample*** into another ***Sample***
    * [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/operationSynthesis.json)](./operation/synthsis) Describes the actions aiming at  realizing a reaction. Should have a ***Reaction*** associated to it.
    * Chromoatography (HPLC, etc.)
    * *Purification?* (Recristallisation, etc.)
    * *Plant extraction?*
    * *etc.* to be worked on!
  * 5 ***Analysis*** provides information about a ***Sample***
    * Spectroscopy
      * NMR [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/analysisNMRspectra.json)](./analysis/NMR) [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/analysisNMRdata.json)](./analysis/NMR) 
      * IR
      * Ms...
    * Non-spectroscopy
      * Melting point
      * *etc.*
    * characterization: 
      * No mimimal property present / red
      * Missing essential property / red
      * image / orange-red
      * propriatary format / orange-red
      * (no green - not other categories otherwise becomes ***Assignment***)
  * 6 ***Assignment*** combines one (or a set of) ***Analysis*** with one (or more) ***Compound***(s) 
    * NMR [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/assignmentNMRspectra.json)](./assignment/NMR) [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/assignmentNMRdata.json)](./assignment/NMR) 
    * IR
    * Ms ? categories...
    * *etc.*
    * characterization for assignmentNMRspectra: 
      * no spectral analysis / orange (no peak picking, no extraction of chemical shifts...)
      * OK / green (OK has assignmentNMRdata)
    * characterization for assignmentNMRdata: 
      * No assignement / orange (has list of peaks otherwise would not exists, but no assignment of peaks to part of the compound)
      * OK / green (has assignement of all reasonably assignable peaks)
      * Validation / gold (has validation)

### Goal 1: Provide a linked-data consolidation of the CHEMeDATA format

Move from the NMR-only assignment format of the NMReDATA initiative (based on .sdf files) towards linked data. <a href="https://json-ld.org/" title="JSON-LD Data"><img style="border:0px;" width="24" src="https://json-ld.org/images/json-ld-data-24.png" alt="JSON-LD-logo-24"/></a>

### Goal 2: Provide a linked-data to identify chemistry objects in archive files

[work-in-progress owl file](chemedata/playground/chemedata.owl)
```
https://chemedata.github.io/ontologies/chemedata/playground/chemedata.owl
```
Exported [OWLDoc](chemedata/playground/index.html) can be found in the chemedata/playground folder.


