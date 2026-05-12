# Results Interpretation

## 1. Molecular Docking Results

Docking was performed against the prepared Andes virus Gc glycoprotein structure. Docking scores were interpreted as predicted binding affinities, with more negative values indicating more favorable predicted binding.

### 1.1 Main Docking Ranking

| Rank | Molecule | Docking score (kcal/mol) | Interpretation |
|---:|---|---:|---|
| 1 | Nafamostat | -9.120 | Strongest docking hit |
| 2 | Berberine | -8.152 | Strong docking, toxicity-limited |
| 3 | Ritonavir | -8.078 | Strong docking, poor ADME/toxicity |
| 4 | Clofazimine | -7.984 | Strong docking, ADME/toxicity limitations |
| 5 | Camostat | -7.981 | Strong pharmacological comparator |
| 6 | Lopinavir | -7.955 | Strong docking, poor ADME |
| 7 | Hesperetin | -7.891 | Good docking and ADME |
| 8 | Apigenin | -7.817 | Best integrated lead candidate |
| 9 | Luteolin | -7.723 | Good docking, toxicity alerts |
| 10 | Niclosamide | -7.691 | Good docking, toxicity/CYP concerns |
| 11 | Resveratrol | -7.585 | Good secondary natural candidate |
| 12 | Curcumin | -7.573 | Good docking, multiple alerts |
| 13 | Baicalein | -7.315 | Good ADME, toxicity concerns |
| 14 | Quercetin | -7.242 | Moderate integrated profile |
| 15 | Kaempferol | -7.240 | Good ADME/ProTox, lower docking |
| 16 | Darunavir | -7.378 | ADME/toxicity limitations |
| 17 | Atazanavir | -7.225 | ADME/toxicity limitations |
| 18 | EGCG | -7.556 | Docking acceptable, ADME limitations |

### 1.2 Interpretation

Nafamostat was the strongest docking hit, with a predicted affinity of -9.120 kcal/mol. However, docking alone was not used to define the final lead. Large molecules such as Ritonavir and Lopinavir may obtain favorable docking scores partly because of their larger contact surface, but this does not necessarily translate into better drug-likeness or safety.

Therefore, docking was considered the first filtering layer, followed by ADME and toxicity-based prioritization.

---

## 2. Binding Pose Analysis

### 2.1 Nafamostat

Nafamostat adopted an extended pose within a surface groove of the Andes virus Gc glycoprotein. The predicted binding region involved residues such as:

```text
TRP865, CYS866, THR938, ARG886, ARG1067, TRP985
```

The pose suggested a combination of aromatic, hydrophobic and polar contacts. Nafamostat therefore represents a strong structural hit. However, its toxicity profile reduced its final priority.

### 2.2 Apigenin

Apigenin showed a favorable docking score of -7.817 kcal/mol and occupied a surface groove involving:

```text
TRP865, CYS866, LEU722, MET879, GLY876, ARG886, ARG1067
```

Several residues overlapped with the Nafamostat binding region, including TRP865, CYS866, ARG886 and ARG1067. This suggests that Apigenin may interact with a similar structural groove of Gc, but through a smaller and more drug-like flavonoid scaffold.

---

## 3. SwissADME Results

### 3.1 Best ADME Profiles

The best SwissADME profiles were observed for:

1. Apigenin
2. Kaempferol
3. Hesperetin
4. Resveratrol

These molecules showed favorable combinations of GI absorption, drug-likeness and medicinal chemistry properties.

### 3.2 Apigenin

Apigenin showed one of the strongest ADME profiles:

| Parameter | Result |
|---|---:|
| Molecular weight | 270.24 g/mol |
| TPSA | 90.90 Å² |
| GI absorption | High |
| Lipinski | 0 violation |
| PAINS | 0 alert |
| Brenk | 0 alert |
| Lead-likeness | Yes |

This profile strongly supported Apigenin as a candidate scaffold.

### 3.3 Resveratrol

Resveratrol showed a very favorable ADME profile:

| Parameter | Result |
|---|---:|
| Molecular weight | 228.24 g/mol |
| TPSA | 60.69 Å² |
| GI absorption | High |
| PAINS | 0 alert |
| Brenk | 1 alert |
| Synthetic accessibility | Favorable |

Resveratrol was therefore considered a strong secondary natural candidate.

### 3.4 Camostat

Camostat showed:

- High GI absorption
- No predicted major CYP inhibition
- No PAINS alerts
- No Lipinski violations

However, its limitations included:

- High TPSA
- 10 rotatable bonds
- 3 Brenk alerts
- Lead-likeness not satisfied

Camostat was therefore interpreted as a strong pharmacological comparator rather than the best final lead.

### 3.5 Nafamostat

Nafamostat showed:

- Lipinski 0 violation
- No PAINS alerts
- No major predicted CYP inhibition

However, it also showed:

- Low predicted GI absorption
- High TPSA
- 3 Brenk alerts

This suggested that Nafamostat may be less suitable as an oral candidate, although parenteral delivery could be considered pharmacologically.

---

## 4. ProTox Results

### 4.1 Nafamostat

Nafamostat showed multiple ProTox alerts:

- Hepatotoxicity: active
- Neurotoxicity: active
- Respiratory toxicity: active
- Carcinogenicity: active
- Mutagenicity: active

This profile strongly reduced the final priority of Nafamostat despite its excellent docking score.

### 4.2 Apigenin

Apigenin showed a more acceptable toxicity profile:

- Hepatotoxicity: inactive
- Neurotoxicity: inactive
- Carcinogenicity: inactive
- Mutagenicity: inactive
- Cytotoxicity: inactive
- Clinical toxicity: inactive

However, Apigenin was predicted active for:

- Nephrotoxicity
- Respiratory toxicity

Therefore, Apigenin is not toxicity-free, but it remains more balanced than Nafamostat.

### 4.3 Resveratrol

Resveratrol was notable because ProTox predicted:

- Respiratory toxicity: inactive
- Carcinogenicity: inactive
- Mutagenicity: inactive
- Cytotoxicity: inactive
- Clinical toxicity: inactive

However, it showed:

- Toxicity class 4
- Nephrotoxicity active
- Weak cardiotoxicity alert
- CYP-related alerts

This makes Resveratrol an important secondary candidate, especially for a project focused on pulmonary disease.

### 4.4 Camostat

Camostat showed:

- Toxicity class 5
- Hepatotoxicity inactive
- Neurotoxicity inactive
- Carcinogenicity inactive
- Mutagenicity inactive
- Cytotoxicity inactive
- CYP metabolism inactive

However, Camostat was predicted active for:

- Nephrotoxicity
- Respiratory toxicity
- Clinical toxicity

This limits its final priority despite its strong docking and favorable CYP profile.

---

## 5. SwissTargetPrediction Results

SwissTargetPrediction was used to investigate predicted human targets of prioritized ligands.

### 5.1 Apigenin

Apigenin showed a multi-target profile involving:

- NOX4
- XDH
- PTGS2
- ESR1 / ESR2
- Kinases
- Enzymes
- Oxidoreductases

This profile suggests potential host-directed relevance in inflammation, oxidative stress and signaling pathways.

### 5.2 Kaempferol

Kaempferol showed a profile close to Apigenin, including:

- NOX4
- XDH
- ALOX5
- AHR
- Kinases
- Transporters

### 5.3 Resveratrol

Resveratrol showed predicted targets including:

- PTGS1 / PTGS2
- ESR1
- PIK3CB
- CYP1A2
- CYP2C9
- CYP3A4

This supports its potential relevance as a host-directed secondary candidate.

### 5.4 Camostat and Nafamostat

Camostat and Nafamostat showed profiles enriched in:

- Proteases
- Coagulation-related targets
- Complement-related targets

This is consistent with their known pharmacological class and supports their role as pharmacological comparators.

---

## 6. Integrated Candidate Ranking

The final ranking was based on docking, ADME, ProTox and SwissTargetPrediction.

| Rank | Molecule | Final Interpretation |
|---:|---|---|
| 1 | Apigenin | Best integrated lead candidate |
| 2 | Resveratrol | Strong secondary candidate; respiratory toxicity inactive |
| 3 | Kaempferol | Natural secondary candidate with favorable ADME/ProTox |
| 4 | Camostat | Strong pharmacological comparator |
| 5 | Nafamostat | Best docking hit but toxicity-limited |
| 6 | Hesperetin | Good docking/ADME, toxicity limitations |
| 7 | Luteolin | Good docking, toxicity alerts |
| 8 | Niclosamide | Good docking, toxicity/CYP concerns |
| 9+ | Ritonavir / Lopinavir / Atazanavir / Darunavir | Good docking but poor ADME/toxicity burden |

---

## 7. Main Interpretation

The most important result is that the best docking score did not correspond to the best integrated candidate.

Nafamostat was the strongest structural docking hit, but its toxicity profile was problematic. In contrast, Apigenin showed a slightly weaker docking score but a much better balance between docking, ADME, toxicity and host-target profile.

Therefore:

```text
Nafamostat = strongest docking hit
Apigenin = best integrated lead candidate
Resveratrol = strong secondary respiratory-relevant candidate
Camostat = pharmacological comparator
```
