# Target Preparation Notes

## Selected Target

**Protein:** Andes virus envelope glycoprotein Gc  
**PDB ID:** 6Y6Q  
**Conformation:** post-fusion  
**Selected chain:** Chain A / Glycoprotein C  
**Purpose:** receptor for molecular docking  

---

## Biological Rationale

The Andes virus Gc glycoprotein was selected because it is involved in viral membrane fusion during entry. Since viral entry is an early and essential step in the infection cycle, Gc represents a rational molecular target for exploratory structure-based virtual screening.

---

## Structural Source

The target structure was obtained from the Protein Data Bank:

```text
PDB ID: 6Y6Q
Structure: Andes virus envelope glycoprotein Gc in post-fusion conformation
```

---

## Preparation Strategy

The original PDB file was processed to create a simplified receptor suitable for docking.

### Raw file

```text
ANDV_Gc_6Y6Q_raw.pdb
```

### Cleaned files

```text
ANDV_Gc_6Y6Q_clean.pdb
ANDV_Gc_6Y6Q_chainA_protein_only.pdb
```

The final receptor used for docking was:

```text
ANDV_Gc_6Y6Q_chainA_protein_only.pdb
```

---

## PyMOL Preparation Commands

The following PyMOL workflow was used to generate the protein-only receptor:

```pymol
delete all
load "ANDV_Gc_6Y6Q_raw.pdb"

remove not polymer.protein
select chain_A, chain A
save "ANDV_Gc_6Y6Q_chainA_protein_only.pdb", chain_A
```

If additional cleaning was required, the following commands were used:

```pymol
remove solvent
remove organic
remove inorganic
```

---

## Rationale for Keeping Chain A Only

Chain A was retained to simplify docking and reduce receptor complexity. This allowed a more manageable and interpretable docking workflow.

Advantages:

- simpler receptor preparation
- reduced docking complexity
- easier binding-site interpretation
- compatible with SwissDock workflow

Limitations:

- possible loss of oligomeric or interface context
- possible loss of quaternary structural effects
- reduced representation of the native viral glycoprotein organization

---

## Heteroatoms and Glycans

Heteroatoms and non-protein components were removed for the initial exploratory docking workflow.

This was done to generate a simplified receptor and avoid preparation errors during SwissDock target processing.

Important limitation:

> Gc is a glycoprotein, and glycans may influence surface accessibility and ligand binding. Removing glycans may expose regions that are less accessible in the native glycosylated protein.

Future improvements should include:

- comparison with glycan-retaining receptor preparation
- docking with a more native glycoprotein representation
- analysis of whether the predicted pocket is glycan-shielded

---

## Structural Limitation

The selected structure 6Y6Q corresponds to a **post-fusion** state of Gc.

This is important because inhibitors of viral entry may ideally bind:

- pre-fusion Gc
- transition-state conformations
- fusion-triggering regions
- conserved membrane-interaction surfaces

Therefore, docking against 6Y6Q should be interpreted as exploratory.

Correct interpretation:

> The docking results identify candidate ligands that may interact with a structural groove of Andes virus Gc, but they do not prove inhibition of viral entry.

---

## Final Receptor Used

```text
ANDV_Gc_6Y6Q_chainA_protein_only.pdb
```

This receptor was used for docking in SwissDock / AutoDock Vina.
