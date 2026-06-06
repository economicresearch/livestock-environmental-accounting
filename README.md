
# Livestock Environmental Accounting

This repository accompanies the manuscript:

> **Demand-Driven Environmental Responsibility in Livestock Systems: Integrating Trade-Linked Land-Use Change and Consumption-Based Accounting**

## Overview

The repository contains two complementary analytical workflows used in the study.

### 1. Trade-Linked Livestock-Related Land-Use-Change Accounting (LUC)

Quantifies livestock-related land-use-change emissions associated with:

- Pasture expansion
- Livestock feed production
- International trade

using:

- Singh et al. (2024) DeDuCE v2.0 hybrid trade-flow dataset
- FAOSTAT Supply Utilization Accounts (SCL)

---

### 2. Consumption-Based Terrestrial Animal-Product Emissions Accounting

Quantifies consumption-based greenhouse-gas emissions associated with:

- Meat products
- Dairy products
- Eggs

using:

- EXIOBASE 3.9.6 environmentally extended MRIO tables
- World Bank population statistics

---

## Repository Structure

```text
livestock-environmental-accounting/

├── README.md
├── requirements.txt
│
├── luc/
│   ├── README.md
│   ├── trade_linked_livestock_LUC_analysis.ipynb
│   ├── data/
│   ├── outputs/
│   └── figures/
│
└── exiobase/
    ├── README.md
    ├── exiobase_terrestrial_animal_product_CBA.ipynb
    ├── data/
    ├── outputs/
    └── figures/
```

---

## Data Availability

Input datasets are not distributed through this repository because of size constraints and third-party licensing requirements.

Instructions for obtaining the required datasets are provided in:

- `luc/README.md`
- `exiobase/README.md`

---

## Reproducibility

The analyses were implemented using documented computational notebooks and reproduce the empirical results reported in the manuscript.

The two analytical components are methodologically distinct and should be interpreted as complementary rather than additive:

1. Trade-linked livestock-related land-use-change accounting
2. Consumption-based terrestrial animal-product emissions accounting

---

## Citation

Citation details will be added following publication.

---

## License

### Code

MIT License.

### Data

Input datasets remain subject to the licenses and terms of use specified by the original data providers, including:

- FAOSTAT
- Singh et al. DeDuCE dataset
- EXIOBASE
- World Bank World Development Indicators

  
