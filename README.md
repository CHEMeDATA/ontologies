## CHEMeDATA ontology

Key formal concepts for annotation of chemistry data

* Basic
  * 1 ***Compound*** [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/compound.json)](./compound)  
    * 2D
    * 3D
  * 2 ***Sample*** [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/sample.json)](./sample) 
* Complex (include basic concepts)
  * 3 ***Reaction*** [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/reaction.json)](./reaction) describes the transformation reactants *Compound*(s) into products *Compound*(s)
  * 4 ***Operation*** transforms a *Sample* into another *Sample*
    * [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/operationReaction.json)](./operation/reaction)
    * Separation
    * Plant extraction
  * 5 ***Analysis*** (of a *Sample*)
    * NMR [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/analysisNMRspectra.json)](./analysis/NMR)  [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/analysisNMRdata.json)](./analysis/NMR) 
    * IR
    * Ms...
  * ***Assignment*** combine *Compound*(s) with *Analysis*
  
*Compound*s are part of a *Sample*s.
*Analysis*s study *Sample*s and say something about *Compound*s.




### Goal 1: Provide a linked-data consolidation of the CHEMeDATA format

Move from the NMR-only assignment format of the NMReDATA initiative (based on .sdf files) towards linked data. <a href="https://json-ld.org/" title="JSON-LD Data"><img style="border:0px;" width="24" src="https://json-ld.org/images/json-ld-data-24.png" alt="JSON-LD-logo-24"/></a>

### Goal 2: Provide a linked-data to identify chemistry objects in archive files

[work-in-progress owl file](chemedata/playground/chemedata.owl)
```
https://chemedata.github.io/ontologies/chemedata/playground/chemedata.owl
```
Exported [OWLDoc](chemedata/playground/index.html) can be found in the chemedata/playground folder.


