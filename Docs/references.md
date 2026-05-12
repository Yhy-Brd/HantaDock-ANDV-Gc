# References

This project relies on public scientific databases, web tools and official public-health resources.

---

## Public Health and Andes Virus Context

1. **CDC — About Andes Virus**  
   The CDC states that there is currently no specific antiviral treatment or vaccine available for Andes virus and that care is centered on supportive management.  
   URL: https://www.cdc.gov/hantavirus/about/andesvirus.html

2. **CDC — 2026 Multi-country Hantavirus Cluster Linked to Cruise Ship**  
   CDC Health Alert Network notice describing the 2026 multi-country hantavirus cluster and confirmation of Andes virus involvement.  
   URL: https://www.cdc.gov/han/php/notices/han00528.html

3. **WHO — Hantavirus cluster linked to cruise ship travel, Multi-country**  
   WHO Disease Outbreak News report describing the cluster of severe respiratory illness associated with hantavirus / Andes virus.  
   URL: https://www.who.int/emergencies/disease-outbreak-news/item/2026-DON600

---

## Target Structure

4. **RCSB PDB — 6Y6Q**  
   Structure of Andes virus envelope glycoprotein Gc in post-fusion conformation.  
   URL: https://www.rcsb.org/structure/6Y6Q

5. **Serris et al. — The Hantavirus Surface Glycoprotein Lattice and Its Fusion Control Mechanism**  
   Structural study describing hantavirus glycoprotein organization and fusion control mechanisms.  
   Linked through the RCSB PDB 6Y6Q record.  
   URL: https://www.rcsb.org/structure/6Y6Q

---

## Docking and Structure Analysis Tools

6. **SwissDock**  
   Online structure-based molecular docking server using docking engines including AutoDock Vina-related workflows.  
   URL: https://www.swissdock.ch/

7. **PyMOL**  
   Molecular visualization software used for receptor inspection, ligand pose visualization and binding-site figure generation.  
   URL: https://pymol.org/

---

## ADME Prediction

8. **SwissADME**  
   Web tool for evaluating physicochemical properties, pharmacokinetics, drug-likeness and medicinal chemistry properties.  
   URL: https://www.swissadme.ch/

9. **Daina A, Michielin O, Zoete V. SwissADME: a free web tool to evaluate pharmacokinetics, drug-likeness and medicinal chemistry friendliness of small molecules.**  
   Scientific Reports. 2017.  
   URL: https://www.nature.com/articles/srep42717

---

## Toxicity Prediction

10. **ProTox 3.0**  
    Webserver for prediction of toxicity of chemicals.  
    URL: https://tox.charite.de/

11. **Banerjee et al. ProTox 3.0: a webserver for the prediction of toxicity of chemicals.**  
    ProTox 3.0 uses molecular similarity and machine-learning models for toxicity endpoint prediction.  
    URL: https://pmc.ncbi.nlm.nih.gov/articles/PMC11223834/

---

## Target Prediction

12. **SwissTargetPrediction**  
    Web tool for predicting likely protein targets of small molecules.  
    URL: http://www.swisstargetprediction.ch/

13. **Daina A, Michielin O, Zoete V. SwissTargetPrediction: updated data and new features for efficient prediction of protein targets of small molecules.**  
    Nucleic Acids Research.  
    URL: https://academic.oup.com/nar/article/47/W1/W357/5494750

---

## Interpretation Notes

- Docking scores should be interpreted as computational predictions, not experimental binding affinities.
- SwissADME, ProTox and SwissTargetPrediction results are predictive and should be validated experimentally.
- The selected target structure 6Y6Q is post-fusion Gc, which is a key limitation for entry-inhibition interpretation.
