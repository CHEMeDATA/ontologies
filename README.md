## CHEMeDATA ontology

Key formal concepts for annotation of chemistry data

* Basic
  * 1 ***Compound*** [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/compound.json)](./compound)  
    * 2D [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/compound2D.json)](./compound)  
    * 3D [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/compound3D.json)](./compound)  
  * 2 ***Sample*** [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/sample.json)](./sample) Different types of samples with different letters
    * (s) Solution sample : Simple solution with a single pure solvent
    * (m) Solution sample in a mixture of solvents: Mixture of solvents
    * (w) Water solution : for water solution with buffer, salt, etc.
    * (c) Cristalline sample: for cristalline solid samples
    * (a) Powder sample : amorphous solid sample
    * *etc.*
* Complex (include basic concepts)
  * 3 ***Reaction*** 
  [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/reaction.json)](./reaction) 
  [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/reaction2.json)](./reaction) describes the transformation of reactants ***Compound***(s) into products ***Compound***(s)
  * 4 ***Operation*** transforms a ***Sample*** into another ***Sample***
    * [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/operationReaction.json)](./operation/reaction) 
    * Separation (HPLC, etc.)
    * Purification (Recristallisation, etc.)
    * Plant extraction
  * 5 ***Analysis*** provides information about a ***Sample***
    * Spectroscopy
      * NMR [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/analysisNMRspectra.json)](./analysis/NMR) [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/analysisNMRdata.json)](./analysis/NMR) 
      * IR
      * Ms...
    * Non-spectroscopy
      * Melting point
  * 6 ***Assignment*** combine ***Compound***(s) with ***Analysis***
     * NMR [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/assignmentNMRspectra.json)](./assignment/NMR) [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/assignmentNMRdata.json)](./assignment/NMR) 
    * IR
    * Ms...


***Compound***s are part of a ***Sample***s.
***Analysis***s study ***Sample***s and say something about ***Compound***s.




### Goal 1: Provide a linked-data consolidation of the CHEMeDATA format

Move from the NMR-only assignment format of the NMReDATA initiative (based on .sdf files) towards linked data. <a href="https://json-ld.org/" title="JSON-LD Data"><img style="border:0px;" width="24" src="https://json-ld.org/images/json-ld-data-24.png" alt="JSON-LD-logo-24"/></a>

### Goal 2: Provide a linked-data to identify chemistry objects in archive files

[work-in-progress owl file](chemedata/playground/chemedata.owl)
```
https://chemedata.github.io/ontologies/chemedata/playground/chemedata.owl
```
Exported [OWLDoc](chemedata/playground/index.html) can be found in the chemedata/playground folder.


