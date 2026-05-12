# Methodology

## 1. Study Design

This project was designed as an exploratory in silico drug discovery mini-project aimed at identifying candidate molecules that may interact with the Andes virus Gc glycoprotein, a viral envelope protein involved in membrane fusion during viral entry.

The workflow integrated:

1. Target selection and protein preparation  
2. Ligand library construction  
3. Molecular docking  
4. Binding pose and residue analysis  
5. ADME prediction  
6. Toxicity prediction  
7. Host-target profiling  
8. Integrated candidate ranking  

The objective was not to validate antiviral activity, but to prioritize candidate ligands for future experimental or computational validation.

---

## 2. Target Selection

### 2.1 Selected Pathogen

The selected pathogen was **Andes virus (ANDV)**, a New World hantavirus associated with hantavirus pulmonary syndrome / hantavirus cardiopulmonary syndrome. This virus is clinically relevant because infection may lead to severe respiratory disease and pulmonary vascular dysfunction.

### 2.2 Selected Molecular Target

The selected molecular target was the **Andes virus Gc glycoprotein**.

The Gc glycoprotein is part of the hantavirus envelope glycoprotein complex and contributes to viral entry through membrane fusion. Because viral entry is an early and essential stage of infection, Gc represents a rational target for exploratory structure-based screening.

### 2.3 Structural Source

The 3D structure used in this study was retrieved from the Protein Data Bank:

- **PDB ID:** 6Y6Q  
- **Target:** Andes virus envelope glycoprotein Gc  
- **Conformation:** post-fusion  
- **Use in this project:** receptor for molecular docking  

### 2.4 Important Structural Limitation

The structure 6Y6Q corresponds to a **post-fusion conformation** of Gc. This is an important limitation because entry inhibitors may ideally target pre-fusion or transition-state conformations. Therefore, docking results were interpreted as exploratory evidence of potential binding rather than proof of entry inhibition.

---

## 3. Protein Preparation

The raw PDB file was downloaded and processed before docking. The preparation consisted of:

1. Loading the PDB structure into PyMOL.
2. Removing water molecules.
3. Removing non-relevant heteroatoms.
4. Retaining the relevant protein chain.
5. Saving a cleaned protein-only receptor file.

The main receptor used for docking was:

```text
ANDV_Gc_6Y6Q_chainA_protein_only.pdb
```

The target preparation strategy is described in detail in:

```text
protein_target/target_preparation_notes.md
```

---

## 4. Ligand Library Construction

A ligand library was assembled from different categories:

1. Antiviral drugs  
2. Entry-related comparators  
3. Repurposed pharmacological compounds  
4. Natural compounds  
5. Flavonoids and polyphenols  

The complete library contained 30 molecules. Among them, 18 molecules were analyzed with the full pipeline: docking + SwissADME + ProTox.

Examples of analyzed ligands include:

- Apigenin
- Resveratrol
- Kaempferol
- Camostat
- Nafamostat
- Hesperetin
- Luteolin
- Niclosamide
- Curcumin
- Baicalein
- Ritonavir
- Lopinavir
- Darunavir
- Atazanavir
- Berberine
- Quercetin
- Clofazimine
- EGCG

SMILES and compound metadata were retrieved from public chemical resources and organized in the ligand library table.

---

## 5. Molecular Docking

### 5.1 Docking Tool

Molecular docking was performed using **SwissDock / AutoDock Vina**.

### 5.2 Docking Strategy

The prepared Andes virus Gc receptor was used as the docking target. Ligands were submitted using their corresponding structures or SMILES. Docking scores were reported in kcal/mol.

More negative values were interpreted as more favorable predicted binding affinities.

### 5.3 Docking Output

For each ligand, the best docking model was recorded. The following information was collected:

- Ligand name
- Docking score
- Model rank
- Visual binding pose
- Binding site location
- Residues surrounding the ligand when available

### 5.4 Binding Pose Analysis

Prioritized ligands were inspected using PyMOL. Residues located within 4 Å of the ligand were identified.

Detailed pose analysis was performed for:

- Nafamostat
- Apigenin

For Apigenin, the binding site involved residues including:

```text
TRP865, CYS866, LEU722, MET879, GLY876, ARG886, ARG1067
```

For Nafamostat, the binding site involved residues including:

```text
TRP865, CYS866, THR938, ARG886, ARG1067, TRP985
```

---

## 6. ADME Prediction

### 6.1 Tool

ADME properties were predicted using **SwissADME**.

### 6.2 Parameters Collected

The following parameters were collected:

- Molecular weight
- TPSA
- Number of hydrogen bond donors
- Number of hydrogen bond acceptors
- Number of rotatable bonds
- Consensus LogP
- Solubility class
- GI absorption
- BBB permeability
- P-gp substrate status
- CYP inhibition
- Lipinski rule
- Ghose rule
- Veber rule
- Egan rule
- Muegge rule
- Bioavailability score
- PAINS alerts
- Brenk alerts
- Lead-likeness
- Synthetic accessibility

### 6.3 ADME Interpretation Criteria

Compounds were considered more favorable when they showed:

- High GI absorption
- No Lipinski violations
- Acceptable TPSA
- No PAINS alerts
- No or few Brenk alerts
- Favorable lead-likeness
- Limited CYP inhibition
- No strong P-gp substrate issue

---

## 7. Toxicity Prediction

### 7.1 Tool

Toxicity was predicted using **ProTox 3.0**.

### 7.2 Parameters Collected

The following toxicity endpoints were evaluated:

- LD50
- Toxicity class
- Hepatotoxicity
- Neurotoxicity
- Nephrotoxicity
- Respiratory toxicity
- Cardiotoxicity
- Carcinogenicity
- Immunotoxicity
- Mutagenicity
- Cytotoxicity
- Clinical toxicity
- CYP-related metabolism endpoints

### 7.3 Toxicity Interpretation Criteria

Compounds were considered less favorable when they showed:

- Low LD50
- Toxicity class 3 or lower
- Active carcinogenicity
- Active mutagenicity
- Active cytotoxicity
- Active hepatotoxicity
- Active neurotoxicity
- Active respiratory toxicity

Because the disease context involves severe pulmonary manifestations, respiratory toxicity was considered an especially important endpoint.

---

## 8. SwissTargetPrediction

### 8.1 Purpose

SwissTargetPrediction was used as a complementary host-target profiling tool.

This analysis was not intended to validate direct binding to Andes virus Gc. Instead, it was used to explore possible human targets, off-targets and host-directed mechanisms of prioritized ligands.

### 8.2 Molecules Analyzed

SwissTargetPrediction was performed for:

- Apigenin
- Resveratrol
- Kaempferol
- Camostat
- Nafamostat

### 8.3 Interpretation

Apigenin and Kaempferol showed multi-target profiles involving enzymes, kinases and oxidative/inflammatory targets. Resveratrol showed targets related to inflammation and host signaling. Camostat and Nafamostat showed profiles enriched in proteases, coagulation and complement-related targets, consistent with their pharmacological classes.

---

## 9. Integrated Ranking

An integrated ranking was generated by combining:

1. Docking affinity
2. Binding pose relevance
3. ADME suitability
4. ProTox toxicity profile
5. SwissTargetPrediction interpretation
6. Biological relevance to viral entry and pulmonary disease

Docking was used to identify structural hits, whereas ADME and ProTox were used to filter molecules with unfavorable pharmacokinetic or safety predictions.

The final interpretation prioritized **Apigenin** as the most balanced candidate.
