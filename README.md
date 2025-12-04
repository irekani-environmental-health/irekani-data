# Irekani Data Repository

> Central data repository for the Irekani Environmental Health Project

[![DOI](https://img.shields.io/badge/DOI-Zenodo-blue.svg)](https://zenodo.org)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![CONACYT](https://img.shields.io/badge/CONACYT-Project%20316204-green.svg)](https://conacyt.mx)

---

## 📖 About This Repository

This repository serves as the central data hub for the **Irekani Environmental Health Project**, a community-based participatory research initiative studying agricultural practices, agrochemical exposure, biodiversity changes, and environmental quality in rural communities of Michoacán, Mexico.

**Irekani** (Purépecha: "health" or "well-being") employs Citizen Science methodologies to document and understand the environmental and health impacts of agrochemical use in agricultural communities.

---

## 📊 Available Datasets

### **1. Complete Dataset (2021-2022)**

**Size**: 288 participants
**Variables**: 181
**Geographic Coverage**: 9 municipalities across 2 lake basins
**Collection Period**: 2021-2022

**Zenodo Repository**: [DOI: pending]

**Includes**:
- Geographic information (2 variables)
- Environmental quality perceptions (20 variables)
- Biodiversity loss records (50 variables)
- Agricultural practices (19 variables)
- Sociodemographic characteristics (9 variables)
- Agrochemical safety practices (11 variables)
- Agrochemical application patterns (4 variables)
- Pest and disease control targets (5 variables)
- Agrochemical compounds used (73 variables)
- Health perceptions and social services (3 variables)

**Documentation**: See [datasets/2023-2024_complete/](datasets/2023-2024_complete/)

---

### **2. Machine Learning Subset (2021-2022)**

**Size**: 127 participants (subset excluding "unknown" health perception responses)
**Use Case**: Health risk prediction modeling
**Zenodo Repository**: [DOI: pending]

This subset filters the complete dataset to include only participants who provided definitive responses ("yes" or "no") regarding perceived health problems related to agrochemical exposure, making it suitable for supervised machine learning classification tasks.

**Related Publication**: Machine learning prediction of health problems from agrochemical exposure (Submitted, 2025)

**Documentation**: See [datasets/2021-2022_ml_subset/](datasets/2021-2022_ml_subset/)

---

## 🗺️ Study Area

**Lake Basins in Michoacán, Mexico**:

### Ciénega de Chapala Basin
- Sahuayo
- Pajacuarán
- Salvador Escalante
- Jiquilpan
- Venustiano Carranza
- Cojumatlán
- Vista Hermosa

### Pátzcuaro-Zirahuén Basin
- Erongarícuaro
- Pátzcuaro

---

## 🔬 Data Collection Methodology

**Approach**: Community-Based Participatory Research (CBPR) / Citizen Science

**Citizen Scientists**: 26 young university students trained in field data collection

**Instruments**:
- Progressive Web App (PWA) for standardized data entry
- Structured interviews with agricultural workers
- Audio recordings and photographic documentation
- GPS location data (anonymized to municipal level)

**Quality Assurance**:
- Training workshops for Citizen Scientists
- Field supervision by research team
- Data validation protocols
- Community verification sessions

**Ethical Considerations**:
- Verbal informed consent from all participants
- Full data anonymization (no personally identifiable information)
- Community engagement throughout the research process
- Results shared with participating communities

See [documentation/collection_methodology.md](documentation/collection_methodology.md) for details.

---

## 🔒 Data Privacy and Anonymization

**Privacy Protection Measures**:
- All participant identifiers removed
- No names, addresses, or exact locations
- Geographic data limited to municipal level only
- No GPS coordinates or community names
- No exact dates of data collection

**Privacy Risk Assessment**: <1%

**Ethics Statement**: This study adhered to the ethical principles of the Declaration of Helsinki. Formal Institutional Review Board (IRB) approval was not obtained as Universidad de La Ciénega del Estado de Michoacán de Ocampo currently lacks an established ethics committee for non-clinical research; however, the study involved minimal risk to participants.

See [documentation/privacy_anonymization.md](documentation/privacy_anonymization.md) for complete details.

---

## 📥 Accessing the Data

### **Primary Data Repository: Zenodo**

All datasets are permanently archived on Zenodo with persistent DOI identifiers:

- **Complete Dataset (n=288)**: [DOI: pending]
- **ML Subset (n=127)**: [DOI: pending]

**File Format**: CSV (UTF-8 encoding)
**License**: Creative Commons Attribution 4.0 International (CC BY 4.0)

### **GitHub Repository**

This repository contains:
- ✅ Dataset documentation and data dictionaries
- ✅ Links to Zenodo datasets
- ✅ Data validation scripts
- ✅ Example analysis notebooks
- ❌ **Raw data files are NOT stored here** (use Zenodo for downloads)

---

## 📖 Data Dictionary

A comprehensive data dictionary with all 181 variables is available in:
- [datasets/2021-2022_complete/data_dictionary.md](datasets/2021-2022_complete/data_dictionary.md)

**Variable Categories**:
1. Geographic Information
2. Environmental Quality Perceptions
3. Biodiversity Loss Records
4. Agricultural Practices
5. Sociodemographic Characteristics
6. Agrochemical Safety Practices
7. Agrochemical Application
8. Pest and Disease Control
9. Agrochemical Compounds Used
10. Health Perceptions and Social Services

---

## 📚 Related Publications

### Published Articles

1. **Martínez-del-Río, A., Iglesias-Mancera, E., Navia-Antezana, J., Yudico-Anaya, L., & Rodríguez-Valencia, A.** (2023). Agrotóxicos y percepción de riesgos, una experiencia de Ciencia Ciudadana en las cuencas Lerma-Chapala y Pátzcuaro-Zirahuén, Michoacán, México. *Trenzar. Revista de Educación Popular, Pedagogía Crítica e Investigación Militante*, (9), 93-106.
   - Repository: [trenzar-glyphosate-assessment](https://github.com/irekani-environmental-health/trenzar-glyphosate-assessment)

### In Review

2. **Yudico-Anaya, L. & Martínez-del-Río, A.E.** (2025). Machine learning prediction of health problems from agrochemical exposure in agricultural workers. *Submitted*.
   - Repository: [agrochemical-health-ml-prediction](https://github.com/irekani-environmental-health/agrochemical-health-ml-prediction)

---

## 📖 How to Cite

### Citing the Dataset

```bibtex
@dataset{yudico2025irekani,
  author       = {Yudico-Anaya, Luis José and
                  Martínez-del-Río, Ana Elisa},
  title        = {Irekani Project: Agricultural Practices,
                  Agrochemical Exposure, and Environmental Quality
                  in Rural Michoacán, Mexico},
  year         = 2025,
  publisher    = {Zenodo},
  version      = {1.0},
  doi          = {[pending]},
  url          = {https://doi.org/10.5281/zenodo.XXXXXX}
}
```

### Citing This Repository

```bibtex
@software{irekani2025data,
  author       = {Yudico-Anaya, Luis José and
                  Martínez-del-Río, Ana Elisa},
  title        = {Irekani Data Repository},
  year         = 2025,
  publisher    = {GitHub},
  url          = {https://github.com/irekani-environmental-health/irekani-data}
}
```

Complete citation metadata: [CITATION.cff](CITATION.cff)

---

## 👥 Project Team

### Principal Investigators

- **Luis José Yudico-Anaya** - Data Science & Machine Learning Lead
  Universidad de La Ciénega del Estado de Michoacán de Ocampo
  📧 ljyudico@ucemich.edu.mx | ljyudico@gmail.com
  🔗 [ORCID: 0000-0002-9304-4304](https://orcid.org/0000-0002-9304-4304)

- **Ana Elisa Martínez del Río** - Public Environmental Health Research Lead
  Universidad de La Ciénega del Estado de Michoacán de Ocampo
  📧 aemartinez@ucemich.edu.mx
  🔗 [ORCID: 0000-0001-7032-0796](https://orcid.org/0000-0001-7032-0796)

### CONACYT Project Collaborators

- Antonio Rodríguez Valencia
- Emma Lorena Iglesias Mancera
- Jaime Fernando Navia-Antezana

### Community Partners

Special recognition to the **288 agricultural workers** and **26 Citizen Scientists** who made this research possible.

---

## 🙏 Acknowledgments

This research was supported by:

- **CONACYT Project 316204**: "Evaluación de los impactos socioambientales del uso de glifosato en las cuencas de Pátzcuaro y Chapala"
- **Universidad de La Ciénega del Estado de Michoacán de Ocampo**
- **Agricultural communities** across 9 municipalities in Michoacán

---

## 📄 License

### Data License

All datasets are released under **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

You are free to:
- Share: copy and redistribute the data
- Adapt: remix, transform, and build upon the data

Under the following terms:
- **Attribution**: You must give appropriate credit and cite the dataset

Full license: https://creativecommons.org/licenses/by/4.0/

### Code License

Scripts and code in this repository are released under the **MIT License**.

See [LICENSE-DATA](LICENSE-DATA) and [LICENSE-CODE](LICENSE-CODE) for details.

---

## 🔗 Related Resources

- [Irekani Environmental Health Project](https://github.com/irekani-environmental-health)
- [CONACYT Project Information](https://conacyt.mx)
- [Universidad de La Ciénega del Estado de Michoacán de Ocampo](https://www.ucemich.edu.mx)
- [Zenodo Community: Irekani Project](https://zenodo.org) (pending)

---

## 📞 Contact

For questions about the data or collaboration inquiries:
- Luis Yudico-Anaya: ljyudico@ucemich.edu.mx
- Ana Elisa Martínez del Río: aemartinez@ucemich.edu.mx

For technical issues with this repository:
- Open an [issue](https://github.com/irekani-environmental-health/irekani-data/issues)

---

## 📅 Version History

**Version 1.0** (2025)
- Initial public release
- Complete dataset (n=288, 181 variables)
- ML subset (n=127)
- Full documentation and data dictionary

---

<div align="center">

**Irekani Environmental Health Project** | CONACYT Project 316204

Universidad de La Ciénega del Estado de Michoacán de Ocampo | Michoacán, Mexico

</div>
