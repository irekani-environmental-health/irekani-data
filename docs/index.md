---
layout: default
title: Irekani Environmental Health Project
description: Agricultural Practices, Agrochemical Exposure, and Environmental Quality in Rural Michoacán, Mexico (2021-2022)
---

# Irekani Environmental Health Project
## Dataset Documentation v1.0

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Dataset](https://img.shields.io/badge/Dataset-288%20participants-blue.svg)](https://github.com/irekani-environmental-health/irekani-data)
[![Variables](https://img.shields.io/badge/Variables-181%20features-green.svg)](datasets/2021-2022_complete/data_dictionary_2021-2022.md)

---

## 📊 Quick Access

<div class="quick-links">
  <a href="#dataset-overview" class="btn">📊 Dataset Overview</a>
  <a href="#documentation" class="btn">📚 Documentation</a>
  <a href="#download" class="btn">⬇️ Download Data</a>
  <a href="#citation" class="btn">📖 How to Cite</a>
</div>

---

## Dataset Overview

The **Irekani Environmental Health Project** provides comprehensive data on agricultural practices, agrochemical exposure, and environmental perceptions in rural Michoacán, Mexico.

### Key Statistics

| Metric | Value |
|--------|-------|
| **Sample Size** | 288 agricultural workers |
| **Variables** | 181 features |
| **Study Period** | 2021-2022 |
| **Location** | Ciénega de Chapala & Pátzcuaro-Zirahuén basins |
| **Original Interviews** | ~500 conducted |
| **Data Quality** | 58% retention rate after validation |

### Research Methodology

- **Approach**: Community-Based Participatory Research (Citizen Science)
- **Citizen Scientists**: 26 trained data collectors
- **Training**: 40-hour intensive course
- **Collection Tool**: Progressive Web App (PWA)
- **Quality Control**: Comprehensive validation and cleaning

---

## Documentation

### Complete Dataset (n=288)

Comprehensive documentation for all 181 variables:

- [📖 Main README](../README.md) - Project overview and context
- [📊 Data Dictionary](../datasets/2021-2022_complete/data_dictionary_2021-2022.md) - Complete variable documentation
- [🔬 Collection Methodology](../documentation/collection_methodology_2021-2022.md) - Field procedures
- [🔒 Privacy & Anonymization](../documentation/privacy_anonymization_2021-2022.md) - Ethical framework

### ML Subset (n=127)

Filtered dataset for machine learning applications:

- [📄 ML Subset README](../datasets/2021-2022_ml_subset/README_ML_SUBSET_2021-2022.md) - Binary classification dataset
- [🤖 Prediction Models](https://github.com/irekani-environmental-health/agrochemical-health-ml-prediction) - Machine learning repository

---

## Variable Categories

The dataset includes 181 variables across 10 major categories:

### 🌍 Environmental Quality (16 variables)
Perceptions of air, water, soil quality, temperature, rainfall patterns, and biodiversity indicators.

### 🐦 Biodiversity Changes (10 variables)
Observations of species abundance (insects, birds, mammals, fish) over time.

### 🌾 Agricultural Practices (15 variables)
Farm size, crop types, years of experience, irrigation methods.

### 👥 Sociodemographic (12 variables)
Age, gender, education, healthcare access, social security.

### 🦺 Safety Practices (25 variables)
Personal Protective Equipment (PPE) use, safety training, equipment maintenance.

### 🚜 Application Patterns (18 variables)
Frequency, timing, methods, dosage, and mixing practices.

### 🐛 Pest Control Targets (7 variables)
Insects, weeds, fungi, rodents targeted by agrochemicals.

### ⚗️ Specific Agrochemicals (73 variables)
Individual compound exposure including glyphosate, atrazine, carbofuran, and others.

### 🏥 Health Perceptions (4 variables)
Perceived health problems and symptom reports (binary outcome variable).

### 📍 Geographic Information (5 variables)
Municipality, lake basin, region identifiers.

---

## Download

### Access on Zenodo

The complete dataset is permanently archived on Zenodo:

- **Complete Dataset (n=288)**: [DOI: pending](https://zenodo.org)
- **ML Subset (n=127)**: [DOI: pending](https://zenodo.org)

### File Formats

- **CSV**: Main data format with UTF-8 encoding
- **Codebook**: PDF and Markdown formats
- **Documentation**: Markdown files

**Note**: Data files are NOT stored in the GitHub repository. All data is available exclusively through Zenodo.

---

## Citation

If you use this dataset in your research, please cite:

### Recommended Citation (APA)

```
Yudico-Anaya, L. J., & Martínez-del-Río, A. E. (2025). Irekani Project:
Agricultural Practices, Agrochemical Exposure, and Environmental Quality
in Rural Michoacán, Mexico [Data set]. Zenodo.
https://doi.org/10.5281/zenodo.XXXXXX
```

### BibTeX

```bibtex
@dataset{yudico2025irekani,
  author       = {Yudico-Anaya, Luis José and
                  Martínez-del-Río, Ana Elisa},
  title        = {Irekani Project: Agricultural Practices,
                  Agrochemical Exposure, and Environmental
                  Quality in Rural Michoacán, Mexico},
  year         = 2025,
  publisher    = {Zenodo},
  version      = {1.0},
  doi          = {10.5281/zenodo.XXXXXX},
  url          = {https://doi.org/10.5281/zenodo.XXXXXX}
}
```

---

## Related Publications

### Published Articles

1. **Martínez-del-Río, A., Iglesias-Mancera, E., Navia-Antezana, J., Yudico-Anaya, L., & Rodríguez-Valencia, A. (2023)**
   *Agrotóxicos y percepción de riesgos, una experiencia de Ciencia Ciudadana en las cuencas Lerma-Chapala y Pátzcuaro-Zirahuén, Michoacán, México*
   Trenzar, Issue 9, pp. 93-106
   [📄 Article Repository](https://github.com/irekani-environmental-health/trenzar-glyphosate-assessment)

### In Peer Review

2. **Yudico-Anaya, L. J., & Martínez-del-Río, A. E. (2025)**
   *Machine learning prediction of health problems from agrochemical exposure*
   Status: Under review
   [🤖 Code Repository](https://github.com/irekani-environmental-health/agrochemical-health-ml-prediction)

---

## Privacy & Ethics

### Anonymization

- **K-anonymity analysis**: Re-identification risk <1%
- No Personally Identifiable Information (PII)
- Geographic precision limited to municipal level
- Dates aggregated to protect privacy

### Ethical Framework

- Helsinki Declaration principles
- Informed consent from all participants
- Community approval secured
- Research use only

### License

**Creative Commons Attribution 4.0 International (CC BY 4.0)**

You are free to:
- ✅ Share and adapt the data
- ✅ Use for any purpose (including commercial)

You must:
- 📖 Cite the dataset appropriately
- 📝 Indicate if changes were made

[Full license details](https://creativecommons.org/licenses/by/4.0/)

---

## Funding

This research was supported by:

- **CONACYT Project 316204**: "Evaluación de los impactos socioambientales del uso de glifosato en las cuencas de Pátzcuaro y Chapala"
- **Universidad de La Ciénega del Estado de Michoacán de Ocampo**

---

## Contact

### Dataset Authors

**Luis José Yudico-Anaya** (Data Science Lead)
📧 ljyudico@ucemich.edu.mx
🔗 [ORCID: 0000-0002-9304-4304](https://orcid.org/0000-0002-9304-4304)

**Ana Elisa Martínez-del-Río** (Public Environmental Health Research Lead)
📧 aemartinez@ucemich.edu.mx
🔗 [ORCID: 0000-0001-7032-0796](https://orcid.org/0000-0001-7032-0796)

### Technical Issues

For technical issues with this repository:
- [Open an issue](https://github.com/irekani-environmental-health/irekani-data/issues)
- [GitHub Discussions](https://github.com/irekani-environmental-health/irekani-data/discussions)

---

## Acknowledgments

We acknowledge:
- **288 agricultural workers** who participated in this study
- **26 Citizen Scientists** who conducted field data collection
- **Communities** in the Pátzcuaro and Lerma-Chapala basins
- **CONACYT** for financial support

---

<div align="center">

**Irekani Environmental Health Organization**

[🏠 Main Repository](https://github.com/irekani-environmental-health/irekani-data) |
[🤖 ML Models](https://github.com/irekani-environmental-health/agrochemical-health-ml-prediction) |
[📄 Published Article](https://github.com/irekani-environmental-health/trenzar-glyphosate-assessment)

Universidad de La Ciénega del Estado de Michoacán de Ocampo | Michoacán, Mexico

*Last updated: December 2025 | Version 1.0*

</div>
