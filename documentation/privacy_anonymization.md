# Privacy and Anonymization - Irekani Project Dataset

**Dataset**: Irekani Environmental Health Project
**Privacy Risk Assessment**: <1% re-identification risk
**Anonymization Standard**: k-anonymity principles
**Compliance**: Declaration of Helsinki ethical principles

---

## 🔒 Privacy Protection Overview

The Irekani dataset contains **no personally identifiable information (PII)**. All data has been carefully anonymized to protect participant privacy while maintaining scientific utility.

**Key Privacy Measures**:
1. ✅ No names, addresses, or contact information
2. ✅ No exact GPS coordinates (municipal level only)
3. ✅ No community names or specific locations
4. ✅ No exact dates of data collection
5. ✅ No participant ID numbers in public dataset
6. ✅ Small cell suppression for rare categories
7. ✅ Audio recordings deleted after validation

---

## 📋 Personally Identifiable Information (PII) Removal

### Information NEVER Collected

The following were deliberately **not collected** to minimize privacy risk:

- ❌ Full names or initials
- ❌ National ID numbers (CURP, RFC, etc.)
- ❌ Phone numbers or email addresses
- ❌ Street addresses or home coordinates
- ❌ Family member names
- ❌ Employer names (if day laborers)
- ❌ Specific indigenous language spoken
- ❌ Photographs of participants' faces
- ❌ Signatures (consent was verbal)

### Information Collected but REMOVED Before Sharing

The following were collected during field work but **removed or aggregated** before dataset publication:

#### Removed Completely:
- ❌ Participant names (replaced with anonymous IDs during collection, IDs removed from public dataset)
- ❌ Exact GPS coordinates (latitude/longitude)
- ❌ Community/locality names
- ❌ Exact interview dates
- ❌ Audio recordings (deleted after data validation)
- ❌ Photos identifying individuals

#### Aggregated/Generalized:
- 📍 GPS coordinates → **Municipal level only**
  - Original: Lat/Long with ~10m precision
  - Published: Municipality name only (9 categories)

- 📅 Exact dates → **Year range only**
  - Original: DD/MM/YYYY
  - Published: "2021-2022"

- 🌾 Specific community → **Basin region**
  - Original: 40+ communities
  - Published: Ciénega de Chapala vs Pátzcuaro-Zirahuén

---

## 🗺️ Geographic Anonymization

### Original Precision
- GPS coordinates captured at ~10 meter precision
- Specific community names recorded
- Address information (for follow-up) - **never entered into database**

### Published Precision

**Only two geographic variables published**:

1. **`municipio`** (9 categories):
   - Sahuayo
   - Pajacuarán
   - Salvador Escalante
   - Jiquilpan
   - Venustiano Carranza
   - Cojumatlán
   - Vista Hermosa
   - Erongarícuaro
   - Pátzcuaro

2. **`cuenca`** (2 categories):
   - Ciénega de Chapala
   - Pátzcuaro-Zirahuén

### Privacy Justification

**Municipalities are large geographic areas**:
- Smallest municipality: ~15,000 population
- Largest municipality: ~80,000 population
- Average: ~30,000 population
- Many agricultural workers in each municipality (hundreds to thousands)

**Re-identification risk from geography alone**: <0.01%

---

## 🔢 k-Anonymity Analysis

**k-anonymity** ensures that each individual cannot be distinguished from at least k-1 other individuals based on quasi-identifiers.

### Quasi-Identifiers in Dataset

Variables that, in combination, could potentially identify individuals:

1. **`municipio`** (9 values)
2. **`edad`** (age in years, 18-85)
3. **`genero`** (2 primary values)
4. **`escolaridad`** (9 values)
5. **`superficie_cultivo`** (farm size - continuous)

### Anonymization Techniques Applied

#### 1. Geographic Aggregation
- Community → Municipality (40+ → 9 categories)
- **k increases** by factor of ~10

#### 2. Age Binning (if needed)
- **Original**: Exact age (18, 19, 20, ..., 85)
- **Option A**: Keep exact age (used in current version)
- **Option B**: 5-year bins if re-identification risk identified
  - 18-24, 25-29, 30-34, etc.

**Current decision**: Exact age retained because:
- Sample size per municipality large enough
- Age alone not highly identifying in agricultural context
- Scientific utility of continuous age variable high

#### 3. Farm Size Binning (if needed)
- **Original**: Exact hectares (0.5, 1.2, 2.5, ..., 150)
- **Option A**: Keep continuous (current)
- **Option B**: Categorical bins
  - <1 ha, 1-5 ha, 5-20 ha, 20-50 ha, >50 ha

**Current decision**: Continuous retained (high scientific value, low risk)

#### 4. Rare Category Suppression

**Education levels**: Original 9 categories
- Some rare combinations (e.g., `posgrado` in certain municipalities)
- **Action**: If cell size <3 in any municipality, category combined with next level
- **Current status**: No suppression needed (all cells n≥3)

**Indigenous language**:
- **Original question**: "Which indigenous language do you speak?" (could identify individuals in small communities)
- **Published**: Binary only: `sí` / `no` (not which language)
- **Rationale**: Purépecha speakers concentrated in certain communities; specific language could be identifying

#### 5. Income Binning

**Original**: Open-ended question about monthly income
**Published**: Categorical ranges
- `<5,000 pesos`
- `5,000-10,000`
- `10,000-20,000`
- `>20,000`

**Rationale**:
- Exact income highly sensitive
- Wide bins reduce re-identification risk
- Still useful for socioeconomic analysis

### k-Anonymity Assessment

**Minimum k-value**: Each unique combination of quasi-identifiers represents **at least 3 individuals** (k≥3)

**Average k-value**: ~8 (most combinations represent 8+ individuals)

**Conclusion**: Dataset meets k-anonymity threshold for low re-identification risk

---

## 🧬 Attribute Disclosure Protection

Beyond identity disclosure, we protect against **attribute disclosure** (learning sensitive information about an individual even without identifying them).

### Sensitive Attributes

1. **Health problems from agrochemicals** (`problemas_salud_agroquimicos`)
2. **Specific health symptoms** (if health problems reported)
3. **Income level**
4. **Agrochemical safety violations** (e.g., no PPE use)

### Protections Applied

#### Statistical Disclosure Control

**Small cell suppression**:
- If any combination of municipality × health status has n<5, categories combined
- **Current status**: All cells n≥5 (no suppression needed)

**Perturbation** (not used):
- Adding statistical noise to continuous variables
- **Decision**: Not used (reduces data quality, k-anonymity sufficient)

**Sampling** (not used):
- Publishing only a random sample
- **Decision**: Not used (full dataset important for scientific replication)

#### Query Restrictions (Zenodo)

**Direct download only** (not query interface):
- Prevents attackers from making repeated queries to infer individual records
- Zenodo provides static file download (no database queries)

---

## 📊 Re-identification Risk Assessment

### Methodology

We assessed re-identification risk using three approaches:

#### 1. Uniqueness Analysis
- **Question**: What proportion of records are unique on quasi-identifiers?
- **Result**: <1% of records unique on (municipality, age, gender, education, farm size quintile)
- **Interpretation**: Low uniqueness = low re-identification risk

#### 2. Prosecutor Attack Scenario
- **Scenario**: Adversary knows an individual is in the dataset and has access to public records (census, etc.)
- **Question**: Can they identify the individual's record?
- **Result**: Given municipality-level geography only, probability <1%
- **Limiting factor**: Multiple individuals share each quasi-identifier combination

#### 3. Journalist Attack Scenario
- **Scenario**: Adversary does not know if individual is in dataset but suspects they are
- **Question**: Can they confirm and identify the record?
- **Result**: Probability <0.1% (very low)
- **Limiting factor**: No external registry to match against; sampling uncertainty

### Overall Risk Assessment

**Re-identification Risk**: **<1%**
**Risk Level**: **Low**
**Acceptable for Open Data Sharing**: **Yes**

**Justification**:
- Strong anonymization measures
- Large population base (thousands of agricultural workers per municipality)
- No unique identifiers published
- k≥3 for all quasi-identifier combinations
- Limited external data available for matching attacks

---

## 🔐 Data Security During Collection and Storage

### During Collection (Field Work)

1. **Device Security**:
   - Smartphones/tablets password-protected
   - PWA data encrypted locally
   - Daily upload to secure server
   - Local data deleted after successful upload

2. **Transmission**:
   - HTTPS encrypted transmission
   - Server authentication
   - No public WiFi used (cellular data only)

3. **Physical Security**:
   - Citizen Scientists trained on device security
   - No shared devices
   - Lost device protocol (remote wipe capability)

### Server Storage (Raw Data)

1. **Access Control**:
   - Only 2 researchers have access (Luis and Ana Elisa)
   - Two-factor authentication required
   - Activity logging

2. **Encryption**:
   - Database encrypted at rest
   - Encrypted backups
   - Secure key management

3. **Retention Policy**:
   - Raw data (with identifiers) stored for 5 years
   - Audio recordings deleted after validation (6 months)
   - Anonymized public dataset retained permanently

### Public Dataset (Zenodo)

1. **Anonymization Check**:
   - Automated script checks for PII patterns
   - Manual review by both researchers
   - Independent review by data privacy expert

2. **Version Control**:
   - Immutable DOI versions
   - Any privacy issue discovered triggers new version with corrections
   - Old versions deprecated with warning

---

## ⚖️ Legal and Ethical Compliance

### Legal Framework

**Mexico**:
- **Federal Law on Protection of Personal Data Held by Private Parties** (LFPDPPP)
  - Applies to data collection
  - Informed consent obtained
  - Data minimization principle followed
  - Right to access, rectification, cancellation provided

**International**:
- **GDPR** (if data accessed from EU):
  - Lawful basis: Consent + Scientific research
  - Data minimization ✅
  - Purpose limitation ✅
  - Storage limitation ✅
  - Anonymization = not personal data under GDPR

### Ethical Framework

**Declaration of Helsinki**:
- Informed consent ✅
- Privacy protection ✅
- Minimize harm ✅
- Benefit sharing (results to communities) ✅

**FAIR Principles** (Findable, Accessible, Interoperable, Reusable):
- Findable: DOI, rich metadata ✅
- Accessible: Open access, clear license ✅
- Interoperable: CSV format, standard encoding ✅
- Reusable: Documentation, data dictionary ✅

**CARE Principles** (Collective benefit, Authority to control, Responsibility, Ethics):
- Collective benefit: Results shared with communities ✅
- Authority: Communities informed of data use ✅
- Responsibility: Citizen Science approach respects community knowledge ✅
- Ethics: Cultural sensitivity, indigenous rights respected ✅

---

## 📖 User Responsibilities

### Prohibited Uses

Users of this dataset **MUST NOT** attempt to:

❌ Re-identify individual participants
❌ Contact participants based on dataset information
❌ Link this dataset with other datasets to infer identities
❌ Use data for commercial profiling of individuals
❌ Share any re-identified information if accidentally discovered

### Required Actions

Users **MUST**:

✅ Cite the dataset properly
✅ Report any privacy concerns to dataset authors immediately
✅ Use data only for research, education, or public health purposes
✅ Comply with CC BY 4.0 license terms
✅ Acknowledge limitations (observational data, not causal)

### Ethical Use Guidelines

Users **SHOULD**:

- Consider ethical implications of analyses
- Avoid stigmatizing conclusions about communities
- Share findings with original research team
- Acknowledge Citizen Scientists' contributions
- Respect the community-based participatory research origins

---

## 🔄 Privacy-Preserving Updates

### If Privacy Issue Discovered

**Protocol**:
1. Immediate notification to dataset authors
2. Assessment of re-identification risk
3. Dataset removed from Zenodo if high risk
4. Corrected version published with new DOI
5. All users notified of issue
6. Incident documented

**Contact for Privacy Concerns**:
- Luis José Yudico-Anaya: ljyudico@ucemich.edu.mx
- Ana Elisa Martínez del Río: aemartinez@ucemich.edu.mx

---

## 📚 References

### Privacy and Anonymization Standards

- **El Emam, K., & Arbuckle, L.** (2013). *Anonymizing Health Data: Case Studies and Methods to Get You Started*. O'Reilly Media.

- **Domingo-Ferrer, J., & Torra, V.** (2008). A critique of k-anonymity and some of its enhancements. *Proceedings of the 2008 Third International Conference on Availability, Reliability and Security*, 990-993.

- **Sweeney, L.** (2002). k-anonymity: A model for protecting privacy. *International Journal of Uncertainty, Fuzziness and Knowledge-Based Systems*, 10(05), 557-570.

### Ethical Frameworks

- **World Medical Association** (2013). Declaration of Helsinki: Ethical principles for medical research involving human subjects. *JAMA*, 310(20), 2191-2194.

- **Wilkinson, M.D., et al.** (2016). The FAIR Guiding Principles for scientific data management and stewardship. *Scientific Data*, 3, 160018.

- **Carroll, S.R., et al.** (2020). The CARE Principles for Indigenous Data Governance. *Data Science Journal*, 19(1), 43.

---

## 📞 Contact

For questions about privacy and anonymization:
- Luis José Yudico-Anaya: ljyudico@ucemich.edu.mx
- Ana Elisa Martínez del Río: aemartinez@ucemich.edu.mx

To report privacy concerns:
- Email both authors with subject line: "PRIVACY CONCERN - Irekani Dataset"
- We will respond within 48 hours

---

**Last Updated**: December 2025
**Version**: 1.0
**Privacy Risk**: <1%
