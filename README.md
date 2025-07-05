![SWIRL logo](Swirl-logo.jpg)

- This dataset was developed as part of the **SWIRL (Stillbirth: When is Risk Low?)** project at the **University of Nottingham**, with support from the *Welcome Leap In Utero* initiative.  
- It contains structured clinical tables, metadata, and multimodal case-level data including imaging and contraction recordings.  
- It is designed for downstream tasks such as predicting the risk of stillbirth, multimodal analysis, and machine learning model training.
---

## Directory Structure

```
SWIRL_data/
├── tables/       # Structured data tables (from Excel sheets)
│ ├── Data_Clinical_Pregnancyevel.csv
│ ├── Data_MRI_DWI.csv
│ └── ...
├── metadata/     # Metadata for the tables (column descriptions, units, etc.)
│ ├── Meta_Clinical_PregnancyLevel.csv
│ └── Meta_PCM_MRI_Contraction_DWI.csv
├── cases/ `Case-level folders with raw modalities·
│ ├── SWIRL_A_01/ # Phase A data, visit once only
│ │ ├── SWIRL_A_01_org.nii.gz
│ │ ├── SWIRL_A_01_contractions_measurements.csv
│ │ └── ...
│ ├── ...
│ ├── SWIRL_B_017/ # Phase B data, contains multiple visit
│ │ ├── visit_1/
│ │ │ ├── SWIRL_B_001_1_org.nii.gz
│ │ │ ├── SWIRL_B_001_1_contractions_measurements.csv
│ │ │ └── ...
│ │ └── ...
│ └── ...
└── README.md     # Dataset description and structure
```

---

## Files Description


### 1. `tables/`
- Contains structured data exported from Excel sheets. Each CSV file corresponds to one data type.
- File descriptions:
  - `Data_Clinical_*.csv`: Clinical datasets, including pregnancy data, ultrasound data, neonatal data, and outcomes (which include the stillbirth risk label, named Near Miss).
  - `Data_PCM.csv`: Uterine contraction analysis from the PCM device.
  - `Data_Math.csv`: Outputs from mathematical biomedical modeling.
  - `Data_Contraction_Manual.csv`: Contraction analysis based on manual inspection of MRI images.
  - `Data_MRI_values.csv`: Features extracted from structural MRI scans.
  - `Data_MRI_DWI.csv`: Diffusion-weighted MRI features.

### 2. `metadata/`
- Each file describes the corresponding data table, including:
  `Variable name`, `Data type`, `Derived variable`, `Variable term`, `Measurement unit`, `Variable Response Options and Feasibility of Values, Derivation hierarchy`, `Comments`
- File descriptions:
  - `Meta_Clinica_*.csv`: Metadata files for clinical data tables. Filenames match the corresponding data files (e.g., `Meta_Clinical_PregnancyLevel.csv` corresponds to `Data_Clinical_PregnancyLevel.csv`).
  - `Meta_PCM_Math_MRI_Contraction_DWI.csv`: A combined metadata file covering the following tables:
    - `Data_PCM.csv`
    - `Data_Math.csv`
    - `Data_Contraction_Mannual.csv`
    - `Data_MRI_values.csv`
    - `Data_MRI_DWI.csv`

### 3. `cases/`
- Contains multimodal data organized by individual cases.
- Each folder includes:
  - `*_org.nii.gz`: 4D dynamic MRI imaging.
  - `*_mask.nii.gz`: 4D mask for the crossbounding MRI image.
  - `*_contractions_measurements.csv`: Case level mannuly checked contraction anylisis
  - `TODO`: add signal data?
---

## Notes

- All personally identifiable information (PII) has been removed or anonymized.
- Column definitions and data types are available in the `metadata/` directory.
- This dataset is for **research use only** and not intended for clinical decision-making.

---

## Contact

For questions or access to raw data modalities, please contact:  
**<your.email@example.com>**
`TODO`

