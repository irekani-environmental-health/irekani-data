# Machine Learning Subset - Irekani Project (2021-2022)

**Dataset Name**: Irekani Project - ML Subset for Health Risk Prediction
**Sample Size**: 127 participants
**Variables**: 181 (same as complete dataset)
**Use Case**: Supervised machine learning for health risk classification

---

## 📊 Dataset Overview

This is a **filtered subset** of the complete Irekani dataset (n=288), specifically prepared for **supervised machine learning** applications in health risk prediction.

### Key Difference from Complete Dataset

The complete dataset includes 288 agricultural workers, but 161 participants responded "desconocido" (unknown) when asked:

> **"¿Cree que el uso de agroquímicos ha causado problemas de salud a usted o su familia?"**
> *("Do you believe agrochemical use has caused health problems for you or your family?")*

**This ML subset includes only the 127 participants who provided definitive responses**:
- **"Sí"** (Yes) - Believes agrochemicals have caused health problems
- **"No"** (No) - Does not believe agrochemicals have caused health problems

This filtering creates a **binary classification target** suitable for supervised machine learning models.

---

## 🎯 Target Variable

### `problemas_salud_agroquimicos`

- **Type**: Binary categorical
- **Values**:
  - `sí` (Yes) - Participant believes agrochemical exposure caused health problems
  - `no` (No) - Participant does not believe agrochemical exposure caused health problems
- **Distribution** (n=127):
  - Class balance details available in related publication

**Research Question**: Can we predict perceived health problems from agrochemical exposure based on agricultural practices, safety behaviors, sociodemographic factors, and environmental perceptions?

---

## 📖 Variable Categories (181 total)

All 181 variables from the complete dataset are included:

1. **Geographic Information** (2 variables)
   - Municipality
   - Lake basin

2. **Environmental Quality Perceptions** (20 variables)
   - Perceived changes in water, air, soil quality
   - Climate pattern changes
   - Biodiversity observations

3. **Biodiversity Loss Records** (50 variables)
   - Species reported as decreased (birds, mammals, reptiles, fish, invertebrates, plants)

4. **Agricultural Practices** (19 variables)
   - Farm size, crops, irrigation
   - Labor practices
   - Economic factors

5. **Sociodemographic Characteristics** (9 variables)
   - Age, gender, education
   - Household size
   - Healthcare access

6. **Agrochemical Safety Practices** (11 variables)
   - PPE use (gloves, masks, protective clothing)
   - Safety training
   - Storage and disposal practices

7. **Agrochemical Application Patterns** (4 variables)
   - Frequency, timing, methods
   - Preventive vs curative use

8. **Pest and Disease Control Targets** (5 variables)
   - Insects, weeds, fungi, rodents

9. **Agrochemical Compounds Used** (73 variables)
   - Specific herbicides, insecticides, fungicides
   - Includes glyphosate and 72 other compounds

10. **Health Perceptions and Social Services** (3 variables)
    - **Target variable**: `problemas_salud_agroquimicos`
    - Symptoms reported
    - Medical access

---

## 🔬 Intended Use Cases

This dataset is designed for:

### ✅ Appropriate Uses

1. **Health Risk Classification Models**
   - Binary classification of perceived health risk
   - Feature importance analysis
   - Model interpretability studies

2. **Public Health Research**
   - Identifying risk factors for health concerns
   - Understanding patterns of agrochemical exposure
   - Evaluating effectiveness of safety practices

3. **Educational Purposes**
   - Teaching supervised learning
   - Demonstrating class imbalance handling
   - Feature engineering examples

4. **Methodological Research**
   - Comparing ML algorithms on real-world data
   - Testing interpretable ML methods
   - Evaluating fairness and bias in health prediction

### ❌ Inappropriate Uses

1. **Medical Diagnosis** - This dataset captures *perceived* health problems, not clinical diagnoses
2. **Individual Risk Prediction** - Data is anonymized and aggregated at municipal level
3. **Regulatory Decision-Making** - Observational data cannot establish causation
4. **Commercial Profiling** - Privacy protections prohibit individual identification

---

## 📥 Data Access

### **Zenodo Repository** (Permanent Archive)

**DOI**: [pending - will be added upon publication]

**Download**: [https://doi.org/10.5281/zenodo.XXXXXX](https://doi.org/10.5281/zenodo.XXXXXX)

**File Format**: CSV (UTF-8 encoding)
**File Size**: ~300 KB
**License**: CC BY 4.0

### **Variable Definitions**

Complete variable descriptions available in:
- [Complete Dataset Data Dictionary](../2021-2022_complete/data_dictionary.md)

---

## 📊 Sample Characteristics

### Geographic Distribution

**Two Lake Basins in Michoacán, Mexico**:

1. **Ciénega de Chapala Basin** (7 municipalities)
   - Sahuayo, Pajacuarán, Salvador Escalante, Jiquilpan
   - Venustiano Carranza, Cojumatlán, Vista Hermosa

2. **Pátzcuaro-Zirahuén Basin** (2 municipalities)
   - Erongarícuaro, Pátzcuaro

### Sociodemographic Profile (n=127)

- **Age range**: 18-85 years
- **Occupation**: Agricultural workers (farmers, day laborers, ejidatarios)
- **Agricultural experience**: 1-70+ years
- **Education levels**: From no formal education to postgraduate
- **Farm sizes**: 0.5 to 100+ hectares

### Agricultural Characteristics

- **Main crops**: Corn, beans, sorghum, wheat, strawberries, avocados, vegetables
- **Farming types**: Rainfed, irrigated, and mixed systems
- **Agrochemical use**: 73 different compounds documented

---

## 🔒 Privacy and Ethics

### Privacy Protections

- **No personally identifiable information (PII)**
- **Geographic precision limited to municipal level** (no GPS, no community names)
- **No exact dates** of data collection
- **Age binning** considered for re-identification risk
- **k-anonymity**: Privacy risk assessment <1%

### Ethical Considerations

- **Informed Consent**: Verbal consent obtained from all participants
- **Community Engagement**: Results shared with participating communities
- **Data Sovereignty**: Community-based participatory research approach
- **Cultural Sensitivity**: Citizen scientists from local communities
- **Declaration of Helsinki**: Ethical principles followed

**Ethics Statement**: This study involved minimal risk to participants. Formal IRB approval was not obtained as Universidad de La Ciénega del Estado de Michoacán de Ocampo currently lacks an established ethics committee for non-clinical research.

---

## 🤖 Machine Learning Considerations

### Class Balance

Check class distribution before modeling:
- May require class balancing techniques (SMOTE, class weights, etc.)
- Consider stratified cross-validation

### Feature Engineering Suggestions

1. **Aggregation of Biodiversity Loss**: Sum total species groups reported as decreased
2. **PPE Compliance Score**: Composite measure of protective equipment use
3. **Agrochemical Exposure Index**: Frequency × number of compounds used
4. **Environmental Degradation Score**: Count of "empeoró" (worsened) perceptions
5. **Categorical Encoding**: Consider target encoding for high-cardinality variables

### Missing Data

- **`NA`**: Not applicable
- **`desconocido`**: Unknown (in predictor variables only; excluded from target)
- **Missing completely at random (MCAR)** vs **missing not at random (MNAR)**: Consider missingness patterns

### Recommended Preprocessing

1. Handle missing values (imputation or indicator variables)
2. Encode categorical variables (one-hot, target, or ordinal encoding)
3. Scale/normalize continuous variables
4. Address class imbalance if present
5. Feature selection to reduce dimensionality (181 variables)

### Model Interpretability

Given the public health application:
- **Interpretable models preferred** (logistic regression, decision trees, rule-based models)
- **Feature importance**: SHAP values, permutation importance
- **Avoid black-box models** without explanation methods

---

## 📚 Related Publication

### In Review

**Yudico-Anaya, L. & Martínez-del-Río, A.E.** (2025). Machine learning prediction of health problems from agrochemical exposure in agricultural workers. *Submitted*.

**Repository**: [agrochemical-health-ml-prediction](https://github.com/irekani-environmental-health/agrochemical-health-ml-prediction)

This repository contains:
- Complete analysis pipeline
- Jupyter notebooks
- Model implementations
- Results and visualizations

---

## 📖 How to Cite

### Citing the ML Subset Dataset

```bibtex
@dataset{yudico2025irekani_ml,
  author       = {Yudico-Anaya, Luis José and
                  Martínez-del-Río, Ana Elisa},
  title        = {Irekani Project: ML Subset for Health Risk
                  Prediction from Agrochemical Exposure},
  year         = 2025,
  publisher    = {Zenodo},
  doi          = {[pending]},
  url          = {https://doi.org/10.5281/zenodo.XXXXXX}
}
```

### Citing the Related Publication

```bibtex
@article{yudico2025ml_health,
  author       = {Yudico-Anaya, Luis José and
                  Martínez-del-Río, Ana Elisa},
  title        = {Machine learning prediction of health problems
                  from agrochemical exposure in agricultural workers},
  journal      = {[Journal name]},
  year         = 2025,
  note         = {In review}
}
```

**Please cite both the dataset and the publication if you use this data.**

---

## 🔄 Dataset Versions

**Current Version**: 1.0 (2025)

This is a **static snapshot** of the 2021-2022 data collection. Future versions (if any) will be published separately on Zenodo with new DOIs.

---

## 📊 Quick Start Example (Python)

```python
import pandas as pd

# Load the dataset
url = "https://doi.org/10.5281/zenodo.XXXXXX"  # Update with actual DOI
df = pd.read_csv(url)

# Check dataset size
print(f"Shape: {df.shape}")  # Should be (127, 181)

# Check target variable
print(df['problemas_salud_agroquimicos'].value_counts())

# Check for missing values
print(df.isnull().sum().sum())

# Basic preprocessing
from sklearn.model_selection import train_test_split

X = df.drop('problemas_salud_agroquimicos', axis=1)
y = df['problemas_salud_agroquimicos']

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y
)
```

---

## 🆘 Frequently Asked Questions

### Why only 127 participants instead of 288?

The 161 excluded participants responded "desconocido" (unknown) to the target variable question. Including them would require semi-supervised or unsupervised methods, which is beyond the scope of the supervised classification task.

### Can I use the complete dataset (n=288) instead?

Yes! The complete dataset is available separately and suitable for:
- Unsupervised learning (clustering, dimensionality reduction)
- Exploratory data analysis
- Descriptive statistics
- Semi-supervised learning approaches

### What about causality?

This is **observational data**, not experimental. Models can identify associations and risk factors but **cannot establish causal relationships**. Perceived health problems may have multiple causes beyond agrochemical exposure.

### How was the data collected?

Community-Based Participatory Research (Citizen Science) approach:
- 26 trained Citizen Scientists (local university students)
- Structured interviews via Progressive Web App
- Audio recordings and photographic documentation
- Field supervision by research team

See [collection methodology documentation](../../documentation/collection_methodology.md) for details.

### Can I access individual-level GPS coordinates?

No. Geographic precision is limited to **municipal level only** to protect participant privacy.

---

## 📞 Contact

### Data Questions
- Luis José Yudico-Anaya: ljyudico@ucemich.edu.mx
- Ana Elisa Martínez del Río: aemartinez@ucemich.edu.mx

### Technical Issues
- GitHub Repository: [irekani-data](https://github.com/irekani-environmental-health/irekani-data)
- Open an [issue](https://github.com/irekani-environmental-health/irekani-data/issues)

---

## 🙏 Acknowledgments

This research was supported by:
- **CONACYT Project 316204**: "Evaluación de los impactos socioambientales del uso de glifosato en las cuencas de Pátzcuaro y Chapala"
- **Universidad de La Ciénega del Estado de Michoacán de Ocampo**
- **127 agricultural workers** who shared their experiences
- **26 Citizen Scientists** who conducted field data collection

---

**Last Updated**: December 2025
**Version**: 1.0
**License**: CC BY 4.0
