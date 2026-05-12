
# HantaDock-ANDV-Gc

**Structure-based virtual screening of candidate inhibitors targeting Andes virus Gc glycoprotein-mediated viral entry**

---

## Overview

Andes virus (ANDV) is a clinically relevant New World hantavirus associated with severe hantavirus pulmonary syndrome / hantavirus cardiopulmonary syndrome. Recent multi-country reports linked to a cruise-ship-associated cluster have renewed attention around Andes virus and severe hantavirus-associated respiratory disease. Importantly, there is currently **no specific antiviral treatment or licensed vaccine available for Andes virus infection**, and clinical management mainly relies on early supportive care.

This project explores whether small molecules may interact with the **Andes virus Gc glycoprotein**, a viral envelope protein involved in membrane fusion during viral entry. The objective is not to claim the discovery of a treatment, but to generate a structured **in silico hypothesis** by integrating docking, ADME prediction, toxicity profiling and host-target prediction.

---

## Project Aim

The aim of this project was to identify and prioritize candidate molecules targeting Andes virus Gc glycoprotein using an exploratory in silico workflow combining:

1. Structure-based molecular docking  
2. Binding pose and residue analysis  
3. SwissADME pharmacokinetic / drug-likeness prediction  
4. ProTox 3.0 toxicity prediction  
5. SwissTargetPrediction host-target profiling  
6. Integrated candidate prioritization  

---

## Scientific Rationale

Hantavirus entry is mediated by envelope glycoproteins **Gn** and **Gc**. Gc is involved in membrane fusion, a critical step allowing viral genome release into host cells after endosomal entry. Because viral entry is an early and essential event in the infection cycle, the Andes virus Gc glycoprotein represents a rational target for exploratory virtual screening.

The structure used in this project was **PDB ID: 6Y6Q**, corresponding to the Andes virus envelope glycoprotein Gc in a post-fusion conformation.

> **Important note:** because 6Y6Q is a post-fusion Gc structure, the results must be interpreted as exploratory. Entry inhibitors may ideally target pre-fusion or transition-state conformations. This project should therefore be considered a hypothesis-generating computational study.

---

## Workflow

```text
Target selection: Andes virus Gc glycoprotein, PDB 6Y6Q
        ↓
Protein preparation: chain A, protein-only cleaned receptor
        ↓
Ligand library construction
        ↓
Docking with SwissDock / AutoDock Vina
        ↓
Binding pose and residue analysis
        ↓
SwissADME filtering
        ↓
ProTox 3.0 toxicity prediction
        ↓
SwissTargetPrediction host-target profiling
        ↓
Integrated ranking and lead prioritization
```

---

## Ligand Library

The ligand library included antiviral drugs, entry-related comparators, repurposed drugs and natural compounds. The complete library contained 30 ligands, with 18 molecules analyzed using the complete pipeline: docking + SwissADME + ProTox.

The analyzed compounds included:

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
- EGCG
- Ritonavir
- Lopinavir
- Darunavir
- Atazanavir
- Berberine
- Quercetin
- Clofazimine

---

## Key Docking Results

Docking was performed against the prepared Andes virus Gc glycoprotein receptor. More negative docking scores indicate more favorable predicted binding.

| Rank | Molecule | Docking score (kcal/mol) | Interpretation |
|---:|---|---:|---|
| 1 | Nafamostat | -9.120 | Strongest docking hit |
| 2 | Berberine | -8.152 | Strong docking, but toxicity concerns |
| 3 | Ritonavir | -8.078 | Strong docking, poor ADME/toxicity profile |
| 4 | Clofazimine | -7.984 | Strong docking, ADME/toxicity limitations |
| 5 | Camostat | -7.981 | Strong pharmacological comparator |
| 6 | Lopinavir | -7.955 | Strong docking, poor ADME profile |
| 7 | Hesperetin | -7.891 | Good docking and ADME, toxicity limitations |
| 8 | Apigenin | -7.817 | Best integrated lead candidate |
| 9 | Luteolin | -7.723 | Good docking, toxicity alerts |
| 10 | Niclosamide | -7.691 | Good docking, toxicity/CYP concerns |
| 11 | Resveratrol | -7.585 | Good natural-compound candidate |
| 12 | Curcumin | -7.573 | Good docking, multiple alerts |
| 13 | Baicalein | -7.315 | Good ADME, toxicity concerns |
| 14 | Quercetin | -7.242 | ADME acceptable, toxicity concerns |
| 15 | Kaempferol | -7.240 | Strong ADME and ProTox profile |
| 16 | Darunavir | -7.378 | ADME/toxicity limitations |
| 17 | Atazanavir | -7.225 | ADME/toxicity limitations |
| 18 | EGCG | -7.556 | Docking acceptable, ADME limitations |

---

## Lead Candidate Interpretation

### Nafamostat

Nafamostat showed the strongest docking affinity against Andes virus Gc glycoprotein. Its predicted pose was located within a surface groove involving residues such as **TRP865, CYS866, THR938, ARG886, ARG1067 and TRP985**.

However, ProTox predicted multiple toxicity alerts for Nafamostat, including hepatotoxicity, neurotoxicity, respiratory toxicity, carcinogenicity and mutagenicity. Therefore, Nafamostat was interpreted as the **strongest structural docking hit**, but it was **deprioritized after toxicity filtering**.

### Apigenin

Apigenin showed a lower but still favorable docking score of **-7.817 kcal/mol**. Its predicted pose occupied a surface groove of Gc involving residues including **TRP865, CYS866, LEU722, MET879, GLY876, ARG886 and ARG1067**. Several of these residues overlapped with the Nafamostat binding region.

Apigenin displayed one of the best SwissADME profiles, including:

- High predicted gastrointestinal absorption
- No Lipinski violations
- No PAINS alerts
- No Brenk alerts
- Favorable lead-likeness
- Acceptable TPSA and molecular weight

ProTox predicted a more acceptable toxicity profile than Nafamostat, although nephrotoxicity and respiratory toxicity alerts remained. Overall, Apigenin was prioritized as the **most balanced integrated lead candidate**.

### Resveratrol

Resveratrol showed a favorable ADME profile and was predicted **inactive for respiratory toxicity** in ProTox. This is particularly relevant in the context of hantavirus-associated pulmonary disease. Its docking score was lower than Apigenin, and ProTox classified it as toxicity class 4 with a weak cardiotoxicity alert. Therefore, Resveratrol was classified as a **strong secondary candidate**.

### Camostat

Camostat showed strong docking and a favorable ADME profile, including high GI absorption and no predicted major CYP inhibition. However, it had high TPSA, 10 rotatable bonds, Brenk alerts and a ProTox respiratory toxicity alert. Camostat was therefore retained as a **strong pharmacological comparator**, especially because its SwissTargetPrediction profile is consistent with protease-related pharmacology.

---

## Integrated Ranking

The final ranking was based on docking affinity, ADME suitability, toxicity prediction and host-target interpretation.

| Final Rank | Molecule | Final Interpretation |
|---:|---|---|
| 1 | **Apigenin** | Best integrated lead candidate |
| 2 | **Resveratrol** | Strong secondary candidate; respiratory toxicity inactive |
| 3 | **Kaempferol** | Natural secondary candidate with strong ADME/ProTox profile |
| 4 | **Camostat** | Strong pharmacological comparator |
| 5 | **Nafamostat** | Best docking hit but toxicity-limited |
| 6 | Hesperetin | Good docking/ADME, toxicity limitations |
| 7 | Luteolin | Good docking, toxicity alerts |
| 8 | Niclosamide | Good docking, toxicity/CYP concerns |
| 9+ | Ritonavir / Lopinavir / Atazanavir / Darunavir | Good docking but poor ADME/toxicity burden |

---

## Main Conclusion

**Nafamostat was the strongest docking hit, but Apigenin was the best integrated lead candidate.**

Apigenin was prioritized because it combined:

- Favorable docking against Andes virus Gc
- Credible binding pose within a Gc surface groove
- Strong SwissADME profile
- No PAINS or Brenk alerts
- Favorable lead-likeness
- More acceptable toxicity prediction than Nafamostat

These results should be interpreted as **computational hypotheses** requiring further validation.

---

## Limitations

This project is exploratory and computational. The main limitations are:

1. Docking does not prove antiviral activity.
2. The selected Gc structure, 6Y6Q, corresponds to a post-fusion conformation.
3. Viral entry involves additional factors such as Gn, PCDH1, integrins, endocytosis and pH-dependent conformational changes.
4. SwissADME, ProTox and SwissTargetPrediction are predictive tools and do not replace experimental validation.
5. No molecular dynamics simulation was performed.
6. No MM/PBSA or MM/GBSA binding energy refinement was performed.
7. No pseudovirus or cell-based antiviral assay was performed.

---

## Future Work

Recommended next steps:

- Molecular dynamics simulation of the Apigenin-Gc complex
- MM/PBSA or MM/GBSA binding energy estimation
- Pocket conservation analysis across hantavirus Gc proteins
- Comparison with other Gc conformations if available
- Redocking using an independent docking tool
- Experimental validation using pseudovirus entry assays
- Cytotoxicity testing in pulmonary/endothelial cell models

---

## Repository Contents

```text
HantaDock-ANDV-Gc/
│
├── README.md
├── docs/
│   ├── methodology.md
│   ├── results_interpretation.md
│   ├── limitations.md
│   └── references.md
│
├── protein_target/
│   └── target_preparation_notes.md
│
├── results/
│   ├── docking_results.csv
│   ├── adme_summary.csv
│   ├── protox_summary.csv
│   ├── swisstarget_summary.csv
│   └── final_integrated_ranking.csv
│
└── figures/
    ├── workflow.png
    ├── top_docking_scores.png
    ├── apigenin_binding_pose.png
    └── integrated_ranking.png
```

---

## Disclaimer

This project is a computational exploratory study. The identified compounds are not validated treatments for Andes virus infection. Experimental validation is required before any biological or therapeutic claim can be made.
