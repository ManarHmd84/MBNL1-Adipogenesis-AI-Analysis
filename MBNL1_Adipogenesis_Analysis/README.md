# 🧬 MBNL1 Adipogenesis Analysis
### AI-Driven Discovery of "Zombie Adipocytes" in Metabolic Syndrome

[![DOI](https://img.shields.io/badge/Conference-ICGM%202026-green)](https://icgm2026.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)

---

## 📋 Overview

This repository contains the computational analysis pipeline for investigating **MBNL1's role in adipocyte insulin resistance**. Using deep learning approaches, we identified that MBNL1 knockdown creates "zombie adipocytes"—cells that store fat normally but fail to respond to insulin due to splicing disruption of key metabolic genes.

**Key Finding:** MBNL1 regulates adipocyte **QUALITY**, not **QUANTITY**.

---

## 🎯 Research Question

> How does MBNL1 loss lead to insulin resistance in adipocytes despite preserved lipid storage capacity?

---

## 🔬 Methods

| Phase | Tool | Purpose | Output |
|-------|------|---------|--------|
| 1 | RNAProt (CNN) | Binding site prediction | 35,997 sites |
| 2 | SpliceAI | Splicing impact prediction | Δ scores |
| 3 | GOATOOLS | Pathway enrichment | GO/KEGG analysis |

### Pipeline Flowchart
```
CLIP-seq Data (GSE39911)
        ↓
   RNAProt CNN Model
   (AUC: 0.59)
        ↓
  35,997 Binding Sites
  (1,368 high-confidence)
        ↓
   SpliceAI Prediction
        ↓
  Splicing Impact Scores
        ↓
   GO/KEGG Enrichment
        ↓
  Insulin Signaling Disruption
  (p = 1.1×10⁻¹⁰)
```

---

## 📊 Key Results

### Binding Sites Distribution
| Gene | Binding Sites | Δ Score | Clinical Impact |
|------|---------------|---------|-----------------|
| INSR | 7,648 | 0.84 | Insulin resistance |
| Pparg | 9,238 | 0.39 | Master regulator loss |
| Plin1 | 1,646 | 0.57 | Lipid storage defect |
| IRS1 | 3,723 | 0.30 | Signal cascade disruption |

### Pathway Enrichment
- **Response to insulin:** p = 1.1×10⁻¹⁰
- **AMPK signaling:** p = 5.2×10⁻¹⁸
- **Type II diabetes:** p = 6.5×10⁻¹¹

---

## 📁 Repository Structure

```
MBNL1-Adipogenesis-Analysis/
│
├── 📓 notebooks/
│   └── MBNL1_Analysis_Pipeline.ipynb
│
├── 📊 data/
│   ├── phase4_integrated_summary.csv
│   └── GO_enrichment_results.txt
│
├── 📈 figures/
│   ├── phase4_final_summary.png
│   ├── go_enrichment_green.png
│   └── model_performance.png
│
├── 📄 README.md
└── 📋 references.md
```

---

## 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/MBNL1-Adipogenesis-Analysis.git

# Install dependencies
pip install rnaprot spliceai goatools pandas numpy matplotlib

# Run analysis (Google Colab recommended)
# Open notebooks/MBNL1_Analysis_Pipeline.ipynb
```

---

## 📚 References

### Computational Tools

1. **SpliceAI**
   > Jaganathan K, et al. (2019). Predicting Splicing from Primary Sequence with Deep Learning. *Cell*, 176(3), 535-548. [DOI: 10.1016/j.cell.2018.12.015](https://doi.org/10.1016/j.cell.2018.12.015)

2. **RNAProt**
   > Uhl M, et al. (2021). RNAProt: an efficient and feature-rich RNA binding protein binding site predictor. *GigaScience*, 10(8), giab054. [DOI: 10.1093/gigascience/giab054](https://doi.org/10.1093/gigascience/giab054)

3. **GOATOOLS**
   > Klopfenstein DV, et al. (2018). GOATOOLS: A Python library for Gene Ontology analyses. *Scientific Reports*, 8, 10872. [DOI: 10.1038/s41598-018-28948-z](https://doi.org/10.1038/s41598-018-28948-z)

### Data Sources

4. **MBNL1 CLIP-seq (GSE39911)**
   > Wang ET, et al. (2012). Transcriptome-wide Regulation of Pre-mRNA Splicing and mRNA Localization by Muscleblind Proteins. *Cell*, 150(4), 710-724. [GEO: GSE39911](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE39911)

### Global Health Statistics

5. **IDF Diabetes Atlas**
   > International Diabetes Federation. *IDF Diabetes Atlas*, 11th ed. Brussels: IDF, 2025. [diabetesatlas.org](https://diabetesatlas.org)

6. **Metabolic Syndrome Trends**
   > Amiri S, et al. (2025). Worldwide trends in metabolic syndrome from 2000 to 2023. *Nature Communications*, 16:67268. [DOI: 10.1038/s41467-025-67268-5](https://doi.org/10.1038/s41467-025-67268-5)

---

## 🏆 Presented At

**ICGM 2026** - International Conference on Genomic Medicine

---

## 👤 Author

**[Your Name]**  
Master's Student, [Your Institution]  
📧 [your.email@example.com]

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Thesis Supervisor: [Name]
- [Your Institution]
- Data providers: GEO, NCBI

---

*If you use this analysis in your research, please cite this repository.*
