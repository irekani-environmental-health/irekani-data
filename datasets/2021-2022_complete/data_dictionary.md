# Data Dictionary - Irekani Complete Dataset (2021-2022)

**Dataset**: Irekani Project - Agricultural Practices, Agrochemical Exposure, and Environmental Quality
**Sample Size**: 288 participants
**Total Variables**: 181
**Collection Period**: 2021-2022
**Geographic Coverage**: 9 municipalities across 2 lake basins in Michoacán, Mexico

---

## Variable Categories Overview

| Category | Variables | Description |
|----------|-----------|-------------|
| Geographic Information | 2 | Municipal location and lake basin |
| Environmental Quality Perceptions | 20 | Community perceptions of environmental changes |
| Biodiversity Loss Records | 50 | Species loss observations across multiple taxa |
| Agricultural Practices | 19 | Farming methods, crops, and land use |
| Sociodemographic Characteristics | 9 | Age, education, household size, etc. |
| Agrochemical Safety Practices | 11 | PPE use, safety training, handling practices |
| Agrochemical Application Patterns | 4 | Frequency, timing, and methods |
| Pest and Disease Control Targets | 5 | Types of agricultural problems addressed |
| Agrochemical Compounds Used | 73 | Specific pesticides, herbicides, fungicides |
| Health Perceptions and Social Services | 3 | Health problems, medical access |

**Total**: 181 variables

---

## 1. Geographic Information (2 variables)

### `municipio`
- **Type**: Categorical
- **Description**: Municipality where the participant works/lives
- **Values**: 9 municipalities
  - Ciénega de Chapala Basin: Sahuayo, Pajacuarán, Salvador Escalante, Jiquilpan, Venustiano Carranza, Cojumatlán, Vista Hermosa
  - Pátzcuaro-Zirahuén Basin: Erongarícuaro, Pátzcuaro
- **Missing values**: None
- **Privacy note**: Geographic precision limited to municipal level only

### `cuenca`
- **Type**: Categorical
- **Description**: Lake basin region
- **Values**:
  - `Ciénega de Chapala` - Chapala Lake Basin
  - `Pátzcuaro-Zirahuén` - Pátzcuaro-Zirahuén Basin
- **Missing values**: None

---

## 2. Environmental Quality Perceptions (20 variables)

These variables capture participants' observations of environmental changes in their communities over recent decades.

### `calidad_agua`
- **Type**: Ordinal
- **Description**: Perceived change in water quality
- **Values**: `mejoró` (improved), `igual` (same), `empeoró` (worsened), `desconocido` (unknown)

### `calidad_aire`
- **Type**: Ordinal
- **Description**: Perceived change in air quality
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `calidad_suelo`
- **Type**: Ordinal
- **Description**: Perceived change in soil quality
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `temperatura`
- **Type**: Ordinal
- **Description**: Perceived change in temperature patterns
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `lluvia`
- **Type**: Ordinal
- **Description**: Perceived change in rainfall patterns
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `sequia`
- **Type**: Ordinal
- **Description**: Perceived change in drought frequency/severity
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `heladas`
- **Type**: Ordinal
- **Description**: Perceived change in frost events
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `granizo`
- **Type**: Ordinal
- **Description**: Perceived change in hail events
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `vientos`
- **Type**: Ordinal
- **Description**: Perceived change in wind patterns
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `inundaciones`
- **Type**: Ordinal
- **Description**: Perceived change in flood frequency/severity
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `disponibilidad_agua`
- **Type**: Ordinal
- **Description**: Perceived change in water availability
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `erosion_suelo`
- **Type**: Ordinal
- **Description**: Perceived change in soil erosion
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `plagas_cultivos`
- **Type**: Ordinal
- **Description**: Perceived change in crop pest pressure
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `enfermedades_cultivos`
- **Type**: Ordinal
- **Description**: Perceived change in crop disease pressure
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `rendimiento_cultivos`
- **Type**: Ordinal
- **Description**: Perceived change in crop yields
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `calidad_productos`
- **Type**: Ordinal
- **Description**: Perceived change in crop quality
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `costo_produccion`
- **Type**: Ordinal
- **Description**: Perceived change in production costs
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `precio_productos`
- **Type**: Ordinal
- **Description**: Perceived change in crop prices
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `biodiversidad_general`
- **Type**: Ordinal
- **Description**: Overall perceived change in biodiversity
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

### `paisaje_natural`
- **Type**: Ordinal
- **Description**: Perceived change in natural landscape
- **Values**: `mejoró`, `igual`, `empeoró`, `desconocido`

---

## 3. Biodiversity Loss Records (50 variables)

Participants reported which species groups have decreased in their communities. Each variable is binary (0 = not reported, 1 = reported as decreased).

### **Birds (Aves)** - 10 species groups

- `perdida_aguilas`: Eagles (Águilas)
- `perdida_garzas`: Herons (Garzas)
- `perdida_patos`: Ducks (Patos)
- `perdida_gallaretas`: Coots (Gallaretas)
- `perdida_colibries`: Hummingbirds (Colibríes)
- `perdida_golondrinas`: Swallows (Golondrinas)
- `perdida_urracas`: Magpies (Urracas)
- `perdida_tordos`: Blackbirds (Tordos)
- `perdida_zanates`: Grackles (Zanates)
- `perdida_aves_otras`: Other birds

### **Mammals (Mamíferos)** - 10 species groups

- `perdida_conejos`: Rabbits (Conejos)
- `perdida_liebres`: Hares (Liebres)
- `perdida_ardillas`: Squirrels (Ardillas)
- `perdida_tlacuaches`: Opossums (Tlacuaches)
- `perdida_zorrillos`: Skunks (Zorrillos)
- `perdida_comadrejas`: Weasels (Comadrejas)
- `perdida_tuzas`: Gophers (Tuzas)
- `perdida_ratas_campo`: Field rats (Ratas de campo)
- `perdida_murcielagos`: Bats (Murciélagos)
- `perdida_mamiferos_otros`: Other mammals

### **Reptiles and Amphibians** - 8 species groups

- `perdida_serpientes`: Snakes (Serpientes)
- `perdida_lagartijas`: Lizards (Lagartijas)
- `perdida_iguanas`: Iguanas
- `perdida_tortugas`: Turtles (Tortugas)
- `perdida_ranas`: Frogs (Ranas)
- `perdida_sapos`: Toads (Sapos)
- `perdida_salamandras`: Salamanders (Salamandras)
- `perdida_reptiles_otros`: Other reptiles/amphibians

### **Fish (Peces)** - 5 species groups

- `perdida_charales`: Silverside fish (Charales)
- `perdida_carpas`: Carp (Carpas)
- `perdida_tilapias`: Tilapia
- `perdida_bagres`: Catfish (Bagres)
- `perdida_peces_otros`: Other fish

### **Invertebrates** - 12 species groups

- `perdida_abejas`: Bees (Abejas)
- `perdida_avispas`: Wasps (Avispas)
- `perdida_mariposas`: Butterflies (Mariposas)
- `perdida_libelulas`: Dragonflies (Libélulas)
- `perdida_grillos`: Crickets (Grillos)
- `perdida_chapulines`: Grasshoppers (Chapulines)
- `perdida_escarabajos`: Beetles (Escarabajos)
- `perdida_catarinas`: Ladybugs (Catarinas)
- `perdida_hormigas`: Ants (Hormigas)
- `perdida_arañas`: Spiders (Arañas)
- `perdida_lombrices`: Earthworms (Lombrices)
- `perdida_invertebrados_otros`: Other invertebrates

### **Plants (Plantas)** - 5 species groups

- `perdida_arboles_nativos`: Native trees
- `perdida_arbustos`: Shrubs
- `perdida_plantas_medicinales`: Medicinal plants
- `perdida_flores_silvestres`: Wildflowers
- `perdida_plantas_otras`: Other plants

**All biodiversity variables are binary**: 0 = not reported, 1 = reported as decreased

---

## 4. Agricultural Practices (19 variables)

### Land Use and Crops

#### `tipo_productor`
- **Type**: Categorical
- **Description**: Type of agricultural producer
- **Values**: `ejidatario` (communal land), `pequeño propietario` (small landowner), `jornalero` (day laborer), `otros`

#### `superficie_cultivo`
- **Type**: Continuous (hectares)
- **Description**: Farm size in hectares
- **Range**: 0.5 - 100+ ha
- **Missing values**: Coded as `NA`

#### `tipo_agricultura`
- **Type**: Categorical (multiple selection possible)
- **Description**: Type of agriculture practiced
- **Values**: `temporal` (rainfed), `riego` (irrigated), `mixto` (mixed)

#### `cultivos_principales`
- **Type**: Text (multiple crops possible)
- **Description**: Main crops grown
- **Common values**: maíz (corn), frijol (beans), sorgo (sorghum), trigo (wheat), fresa (strawberry), aguacate (avocado), berries, hortalizas (vegetables)

#### `años_experiencia`
- **Type**: Continuous (years)
- **Description**: Years of agricultural experience
- **Range**: 1 - 70+ years

#### `rotacion_cultivos`
- **Type**: Binary
- **Description**: Practices crop rotation
- **Values**: `sí`, `no`, `desconocido`

#### `uso_abonos_organicos`
- **Type**: Binary
- **Description**: Uses organic fertilizers
- **Values**: `sí`, `no`, `desconocido`

#### `uso_fertilizantes_quimicos`
- **Type**: Binary
- **Description**: Uses chemical fertilizers
- **Values**: `sí`, `no`, `desconocido`

#### `sistema_riego`
- **Type**: Categorical
- **Description**: Irrigation system used
- **Values**: `goteo` (drip), `aspersión` (sprinkler), `gravedad` (gravity/flood), `ninguno` (none), `mixto`

#### `fuente_agua_riego`
- **Type**: Categorical (multiple possible)
- **Description**: Water source for irrigation
- **Values**: `pozo` (well), `río` (river), `lago` (lake), `presa` (dam), `lluvia` (rain only)

### Labor and Economics

#### `mano_obra`
- **Type**: Categorical
- **Description**: Type of labor used
- **Values**: `familiar` (family), `contratada` (hired), `mixta` (mixed)

#### `trabajadores_temporada`
- **Type**: Integer
- **Description**: Number of seasonal workers employed
- **Range**: 0 - 100+

#### `ingreso_mensual_agricultura`
- **Type**: Ordinal (categorical ranges)
- **Description**: Monthly income from agriculture
- **Values**: `<5000`, `5000-10000`, `10000-20000`, `>20000` (Mexican pesos)
- **Privacy note**: Binned to protect individual privacy

#### `actividades_economicas_complementarias`
- **Type**: Binary
- **Description**: Has additional economic activities beyond agriculture
- **Values**: `sí`, `no`

### Agricultural Challenges

#### `principal_problema_agricola`
- **Type**: Categorical (open-ended, later coded)
- **Description**: Main agricultural problem faced
- **Common values**: plagas, clima, precios bajos, falta de agua, costos altos

#### `perdidas_cosecha_ultimo_año`
- **Type**: Binary
- **Description**: Experienced significant crop losses in past year
- **Values**: `sí`, `no`, `desconocido`

#### `causa_perdidas`
- **Type**: Categorical (if perdidas = sí)
- **Description**: Main cause of crop losses
- **Values**: `plagas`, `enfermedades`, `clima`, `sequía`, `heladas`, `otros`

### Knowledge and Training

#### `capacitacion_agricola`
- **Type**: Binary
- **Description**: Has received agricultural training
- **Values**: `sí`, `no`

#### `tipo_capacitacion`
- **Type**: Categorical (multiple possible, if capacitacion = sí)
- **Description**: Type of training received
- **Values**: `gobierno`, `universidad`, `privada`, `ONG`, `otros productores`

---

## 5. Sociodemographic Characteristics (9 variables)

### `edad`
- **Type**: Integer (years)
- **Description**: Age of participant
- **Range**: 18 - 85 years
- **Missing values**: Coded as `NA`

### `genero`
- **Type**: Categorical
- **Description**: Gender
- **Values**: `masculino`, `femenino`, `otro`, `prefiere_no_decir`

### `escolaridad`
- **Type**: Ordinal
- **Description**: Educational level
- **Values**: `sin_escolaridad`, `primaria_incompleta`, `primaria`, `secundaria`, `preparatoria`, `técnica`, `universidad_incompleta`, `universidad`, `posgrado`

### `estado_civil`
- **Type**: Categorical
- **Description**: Marital status
- **Values**: `soltero`, `casado`, `unión_libre`, `divorciado`, `viudo`

### `tamaño_hogar`
- **Type**: Integer
- **Description**: Number of people in household
- **Range**: 1 - 12+

### `dependientes_menores`
- **Type**: Integer
- **Description**: Number of children under 18 in household
- **Range**: 0 - 10+

### `posicion_hogar`
- **Type**: Categorical
- **Description**: Position in household
- **Values**: `jefe_familia`, `cónyuge`, `hijo/a`, `otro_familiar`, `otro`

### `acceso_servicios_salud`
- **Type**: Categorical (multiple possible)
- **Description**: Type of health service access
- **Values**: `IMSS`, `ISSSTE`, `Seguro_Popular`, `privado`, `ninguno`

### `idioma_indigena`
- **Type**: Binary
- **Description**: Speaks indigenous language
- **Values**: `sí`, `no`
- **Note**: Specific language not recorded to protect privacy

---

## 6. Agrochemical Safety Practices (11 variables)

### Personal Protective Equipment (PPE)

#### `usa_epp`
- **Type**: Binary
- **Description**: Uses any personal protective equipment
- **Values**: `sí`, `no`, `a_veces`

#### `guantes`
- **Type**: Binary
- **Description**: Uses gloves when handling agrochemicals
- **Values**: `sí`, `no`, `a_veces`

#### `mascarilla`
- **Type**: Binary
- **Description**: Uses respiratory protection (mask/respirator)
- **Values**: `sí`, `no`, `a_veces`

#### `lentes_proteccion`
- **Type**: Binary
- **Description**: Uses protective eyewear
- **Values**: `sí`, `no`, `a_veces`

#### `botas`
- **Type**: Binary
- **Description**: Uses boots when applying agrochemicals
- **Values**: `sí`, `no`, `a_veces`

#### `overol_ropa_protectora`
- **Type**: Binary
- **Description**: Uses protective clothing/coveralls
- **Values**: `sí`, `no`, `a_veces`

### Safety Knowledge and Training

#### `capacitacion_uso_agroquimicos`
- **Type**: Binary
- **Description**: Has received training on safe agrochemical use
- **Values**: `sí`, `no`

#### `lee_etiquetas`
- **Type**: Binary
- **Description**: Reads product labels before use
- **Values**: `siempre`, `a_veces`, `nunca`

#### `respeta_dosis_recomendadas`
- **Type**: Binary
- **Description**: Follows recommended application doses
- **Values**: `siempre`, `a_veces`, `nunca`

### Disposal and Storage

#### `almacenamiento_seguro`
- **Type**: Binary
- **Description**: Stores agrochemicals in secure location
- **Values**: `sí`, `no`, `parcialmente`

#### `disposicion_envases`
- **Type**: Categorical
- **Description**: How empty agrochemical containers are disposed
- **Values**: `programa_recoleccion` (collection program), `quema` (burning), `entierra` (burial), `basura_comun` (regular trash), `reutiliza` (reuses), `otros`

---

## 7. Agrochemical Application Patterns (4 variables)

### `frecuencia_aplicacion`
- **Type**: Ordinal
- **Description**: How often agrochemicals are applied per crop cycle
- **Values**: `nunca`, `1-2_veces`, `3-5_veces`, `6-10_veces`, `más_de_10_veces`

### `momento_aplicacion`
- **Type**: Categorical (multiple possible)
- **Description**: When agrochemicals are applied
- **Values**: `preventivo` (preventive), `curativo` (curative), `ambos` (both)

### `metodo_aplicacion`
- **Type**: Categorical (multiple possible)
- **Description**: Application method
- **Values**: `aspersión_manual` (manual spraying), `aspersión_mecanizada` (mechanized spraying), `riego` (through irrigation), `polvo` (dust/powder), `granular` (granular), `otros`

### `epoca_aplicacion`
- **Type**: Categorical (multiple possible)
- **Description**: Season/period of application
- **Values**: `siembra` (planting), `crecimiento` (growth), `floración` (flowering), `fructificación` (fruiting), `cosecha` (harvest), `todo_el_ciclo` (entire cycle)

---

## 8. Pest and Disease Control Targets (5 variables)

Each variable indicates whether agrochemicals are used to control that category.

### `control_insectos`
- **Type**: Binary
- **Description**: Uses agrochemicals to control insects
- **Values**: `sí`, `no`

### `control_malezas`
- **Type**: Binary
- **Description**: Uses herbicides to control weeds
- **Values**: `sí`, `no`

### `control_hongos`
- **Type**: Binary
- **Description**: Uses fungicides to control fungi/diseases
- **Values**: `sí`, `no`

### `control_roedores`
- **Type**: Binary
- **Description**: Uses rodenticides
- **Values**: `sí`, `no`

### `control_otros`
- **Type**: Binary
- **Description**: Uses agrochemicals for other purposes
- **Values**: `sí`, `no`

---

## 9. Agrochemical Compounds Used (73 variables)

All variables in this category are binary (0 = not used, 1 = used).

Participants reported which specific agrochemical products they use. The list includes herbicides, insecticides, fungicides, and other pesticides commonly available in the region.

### **Herbicides** (includes glyphosate and others)

- `glifosato`: Glyphosate (most commonly reported)
- `paraquat`: Paraquat
- `2_4_d`: 2,4-D
- `atrazina`: Atrazine
- `picloram`: Picloram
- `glufosinato_amonio`: Glufosinate-ammonium
- `ametrina`: Ametryn
- `metolacloro`: Metolachlor
- `pendimetalina`: Pendimethalin
- `otros_herbicidas`: Other herbicides not listed

### **Insecticides**

- `clorpirifos`: Chlorpyrifos
- `metamidofos`: Methamidophos
- `malation`: Malathion
- `cipermetrina`: Cypermethrin
- `deltametrina`: Deltamethrin
- `lambda_cihalotrina`: Lambda-cyhalothrin
- `imidacloprid`: Imidacloprid
- `tiametoxam`: Thiamethoxam
- `fipronil`: Fipronil
- `abamectina`: Abamectin
- `otros_insecticidas`: Other insecticides

### **Fungicides**

- `mancozeb`: Mancozeb
- `captan`: Captan
- `azufre`: Sulfur
- `cobre`: Copper-based fungicides
- `benomilo`: Benomyl
- `tiabendazol`: Thiabendazole
- `carbendazim`: Carbendazim
- `propiconazol`: Propiconazole
- `tebuconazol`: Tebuconazole
- `otros_fungicidas`: Other fungicides

### **Rodenticides**

- `bromadiolona`: Bromadiolone
- `brodifacoum`: Brodifacoum
- `fosfuro_zinc`: Zinc phosphide
- `otros_rodenticidas`: Other rodenticides

### **Fertilizers (Chemical)**

- `urea`: Urea
- `sulfato_amonio`: Ammonium sulfate
- `nitrato_amonio`: Ammonium nitrate
- `fosfato_diamonico`: Diammonium phosphate (DAP)
- `triple_17`: 17-17-17 NPK
- `otros_fertilizantes`: Other chemical fertilizers

### **Growth Regulators and Others**

- `acido_giberelico`: Gibberellic acid
- `ethephon`: Ethephon
- `paclobutrazol`: Paclobutrazol
- `otros_reguladores`: Other growth regulators

**Note**: The complete list includes 73 specific compounds. Each is coded as binary (0 = not used, 1 = used by that participant).

**Important**: Commercial product names were standardized to active ingredients for analysis.

---

## 10. Health Perceptions and Social Services (3 variables)

### `problemas_salud_agroquimicos`
- **Type**: Categorical
- **Description**: Believes agrochemical use has caused health problems for themselves or family
- **Values**: `sí`, `no`, `desconocido`
- **Note**: This is the target variable for the machine learning subset (n=127 excludes "desconocido")

### `sintomas_reportados`
- **Type**: Text (coded categorically)
- **Description**: Specific health symptoms reported (if problemas_salud = sí)
- **Common values**: `dolor_cabeza` (headache), `mareos` (dizziness), `nauseas`, `irritacion_piel` (skin irritation), `problemas_respiratorios` (respiratory), `problemas_oculares` (eye problems), `fatiga`, `otros`
- **Multiple symptoms possible**

### `acceso_medico_ultimo_año`
- **Type**: Binary
- **Description**: Visited a doctor in the past year
- **Values**: `sí`, `no`, `desconocido`

---

## Missing Data Conventions

- **`NA`**: Not applicable or question not asked
- **`desconocido`**: Participant did not know the answer
- **Empty/blank**: Participant declined to answer

---

## Data Quality Notes

1. **Language**: All original responses were in Spanish. This data dictionary provides English translations for international use.

2. **Standardization**:
   - Agrochemical names standardized to active ingredients
   - Municipality names use official INEGI conventions
   - Dates removed to protect privacy

3. **Geographic Precision**: Limited to municipal level only (no GPS coordinates, no community names)

4. **Categorical Responses**: Many open-ended questions were later coded into categories for analysis

5. **Multiple Selection Variables**: Some questions allowed multiple responses (e.g., crops grown, health symptoms)

---

## Citation

When using this dataset, please cite:

```bibtex
@dataset{yudico2025irekani,
  author       = {Yudico-Anaya, Luis José and
                  Martínez-del-Río, Ana Elisa},
  title        = {Irekani Project: Agricultural Practices,
                  Agrochemical Exposure, and Environmental Quality
                  in Rural Michoacán, Mexico},
  year         = 2025,
  publisher    = {Zenodo},
  doi          = {[pending]},
  url          = {https://doi.org/10.5281/zenodo.XXXXXX}
}
```

---

## Contact

For questions about variable definitions or data collection methodology:
- Luis José Yudico-Anaya: ljyudico@ucemich.edu.mx
- Ana Elisa Martínez del Río: aemartinez@ucemich.edu.mx

---

**Last Updated**: December 2025
**Version**: 1.0
