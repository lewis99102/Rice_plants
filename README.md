# Rice_plants
# Dataset for: [Temporal Dynamics of Genotype-Phenotype Correlations from Time Series Rice Plant Data]

The dataset consists of **four data files**, including one phenotype dataset and three genotype-related datasets.  
Phenotype and genotype information can be linked at the **cultivar level**.

---

## Overview of Datasets

The datasets are organized into **two categories**:

- **Phenotype data** (1 file)
- **Genotype data** (3 files)

### Summary

| Category | Dataset name | Description |
|--------|--------------|-------------|
| Phenotype | Phenotype | Time-series phenotypic traits |
| Genotype | SNP_matrix | SNP genotype matrix |
| Genotype | Cultivar | Cultivar index and labeling information |
| Genotype | Sequence_info | Sequence information corresponding to SNPs |

---

## 1. Phenotype

### Description
The phenotype dataset contains **time-dependent phenotypic measurements** for rice cultivars.

- Number of cultivars: **96**
- Samples per cultivar: **4**
- Number of phenotypic traits: **16**
- Data type: **longitudinal (time-series)**

Each cultivar is identified using its **Korean cultivar name** (`Cultivar`).


## 2. SNP_matrix

### Description
This dataset provides the **single nucleotide polymorphism (SNP) genotype matrix** for the cultivars.

- Rows: SNP loci
- Columns: cultivars indexed by numeric identifier
- Values: genotype encoding for each SNP

Cultivar indices correspond to the numeric identifiers defined in the **Cultivar dataset**.

## 3. Cultivar

### Description
This dataset serves as the **link between phenotype and genotype data**.

### Key Columns
- `No.`: Numeric cultivar index used in genotype datasets
- `Cultivar`: Cultivar name (Korean), used in the phenotype dataset

### Usage
- Phenotype data uses `Cultivar` (Korean name)
- Genotype data uses `No.` (numeric index)

By matching these two identifiers, phenotype and genotype data can be integrated.

---

## 4. Sequence_info

### Description
This dataset contains **sequence-level information** associated with SNPs in the SNP matrix.

- Provides metadata for SNP positions
- Enables biological interpretation of genotype variation

Each SNP in `SNP_matrix` corresponds to an entry in `Sequence_info`.
