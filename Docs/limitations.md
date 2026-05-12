# Limitations

This project is an exploratory in silico study. The results should be interpreted as computational hypotheses, not as experimental proof of antiviral activity.

---

## 1. Docking Does Not Prove Antiviral Activity

Molecular docking predicts a possible interaction between a ligand and a protein structure. It does not prove that the ligand:

- binds experimentally to the target
- inhibits viral entry
- blocks membrane fusion
- reduces viral replication
- improves disease outcomes

The identified molecules must therefore be considered **candidate hypotheses**, not validated antivirals.

---

## 2. Use of a Post-Fusion Gc Structure

The selected structure, **PDB 6Y6Q**, corresponds to the Andes virus Gc glycoprotein in a **post-fusion conformation**.

This is a major limitation because entry inhibitors may ideally target:

- pre-fusion Gc
- fusion-intermediate states
- receptor-binding or fusion-triggering regions
- conformational transition interfaces

Therefore, docking against 6Y6Q is useful for identifying possible binding pockets or structural grooves, but it may not fully reflect the biologically optimal conformation for entry inhibition.

---

## 3. Viral Entry Is Multifactorial

Andes virus entry does not depend only on Gc. Viral entry may involve:

- Gn/Gc glycoprotein complex organization
- receptor engagement
- PCDH1 and other host factors
- integrins
- endocytosis
- endosomal pH
- conformational rearrangements
- membrane fusion dynamics

Therefore, a ligand predicted to bind Gc may not necessarily block entry in a biological system.

---

## 4. Protein Preparation Can Influence Docking

Protein preparation choices can affect docking results, including:

- retaining only chain A
- removing glycans
- removing heteroatoms
- using a protein-only receptor
- using a specific conformation
- defining a search space

Since Gc is a glycoprotein, glycans may influence ligand accessibility or surface topology. This project used a simplified protein-only receptor for exploratory docking.

---

## 5. Docking Scoring Has Known Limitations

Docking scores are approximate and may be influenced by:

- ligand size
- ligand flexibility
- scoring function bias
- search box definition
- receptor rigidity
- lack of solvent effects
- lack of membrane context
- absence of protein conformational dynamics

Large molecules may obtain favorable docking scores because of larger contact surfaces, even if their ADME or toxicity profiles are unfavorable.

---

## 6. No Molecular Dynamics Simulation

This project did not include molecular dynamics simulations.

Therefore, the stability of ligand-Gc complexes over time was not evaluated. Future work should include:

- RMSD analysis
- RMSF analysis
- hydrogen bond persistence
- binding site stability
- ligand displacement analysis
- solvent-accessible surface evaluation

---

## 7. No Binding Free Energy Refinement

This project did not perform MM/PBSA or MM/GBSA analysis.

Docking scores were used as an initial ranking tool, but binding free energy refinement would strengthen the interpretation of the top complexes.

---

## 8. ADME Predictions Are Computational

SwissADME provides predicted pharmacokinetic and drug-likeness properties. These predictions do not replace:

- experimental solubility testing
- permeability assays
- metabolic stability assays
- pharmacokinetic profiling
- formulation studies

For example, Nafamostat showed low predicted GI absorption, but this mainly limits oral administration and does not necessarily exclude parenteral delivery.

---

## 9. ProTox Predictions Are Computational

ProTox 3.0 provides predicted toxicity endpoints. These results are useful for early prioritization, but they do not replace:

- in vitro cytotoxicity assays
- hepatotoxicity assays
- respiratory cell toxicity models
- cardiotoxicity studies
- animal toxicology
- clinical safety data

Predicted respiratory toxicity was considered important in this project because Andes virus disease is associated with severe pulmonary manifestations. However, this prediction requires experimental confirmation.

---

## 10. SwissTargetPrediction Does Not Validate Viral Binding

SwissTargetPrediction predicts likely human targets of small molecules based on chemical similarity. It does not validate direct binding to Andes virus Gc.

In this project, SwissTargetPrediction was used only as a complementary tool to explore:

- human off-targets
- host-directed mechanisms
- inflammation-related targets
- metabolism-related risks
- protease/coagulation-related pharmacology

---

## 11. No Experimental Validation

No experimental validation was performed. The following experiments would be required to validate the computational hypotheses:

- pseudovirus entry assay
- live-virus infection assay under appropriate biosafety conditions
- cell viability / cytotoxicity assay
- pulmonary or endothelial cell model testing
- binding assay or biophysical validation
- dose-response antiviral evaluation

---

## 12. Final Interpretation Limitation

Apigenin was prioritized as the most balanced in silico lead candidate. However, this does not mean Apigenin is an antiviral treatment for Andes virus. It means that, among the tested molecules, Apigenin showed the best integrated computational profile.

The correct interpretation is:

> Apigenin is a prioritized in silico candidate requiring further computational and experimental validation.
