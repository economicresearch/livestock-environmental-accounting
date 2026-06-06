
# Trade-Linked Livestock-Related Land-Use-Change Accounting (2018–2022)

This workflow reproduces the analysis of livestock-related land-use-change (LUC) emissions associated with:

- Livestock feed production
- Pasture expansion
- International trade

using:

1. FAOSTAT Supply Utilization Accounts (SCL)
2. Singh et al. (2024) DeDuCE v2.0 hybrid trade-flow dataset

The analysis is implemented in:

```text
trade_linked_livestock_LUC_analysis.ipynb
```

---

# Folder Structure

```text
luc/

├── trade_linked_livestock_LUC_analysis.ipynb
│
├── data/
│   ├── FAOSTAT_crops_feed_data.csv
│   └── Singh_trade_flow_LUC_2018_2022.xlsx
│
├── outputs/
│
└── figures/
```

---

# Input Data

## 1. FAOSTAT Supply Utilization Accounts (SCL)

Official portal:

https://www.fao.org/faostat/en/#data/SCL

### Download settings

Years:

- 2018–2022

Countries:

- All countries

Elements:

- Food
- Feed
- Seed
- Processing
- Loss
- Other uses (non-food)
- Residuals
- Tourist Consumption

Items:

### Cereals and oilseeds

- Soybeans
- Rapeseed
- Sunflower seed
- Maize
- Barley
- Sorghum

### Oilseed cakes

- Cake of soybeans
- Cake of rapeseed
- Cake of sunflower seed

Download as CSV and save as:

```text
luc/data/FAOSTAT_crops_feed_data.csv
```

---

## 2. Singh et al. (2024) DeDuCE v2.0

Official dataset:

https://zenodo.org/records/10633818

Download:

```text
Commodity-driven deforestation, associated carbon emissions and trade 2001–2022.xlsx
```

Retain:

```text
Trade flows--hybrid
```

Filter:

```text
2018–2022
```

Save as:

```text
luc/data/Singh_trade_flow_LUC_2018_2022.xlsx
```

---

# Method Summary

The analysis estimates:

```text
LUC_total = LUC_feed + LUC_pasture
```

Feed-related emissions are estimated as:

```text
LUC_feed = LUC_Singh × Feed Share
```

Feed shares are reconstructed from FAOSTAT:

```text
Feed Share =
Feed /
(Food + Feed + Seed + Processing + Loss +
Other Uses + Residuals + Tourist Consumption)
```

Oilseed meal quantities are converted to seed-equivalent feed using:

- Soybeans = 0.80
- Rapeseed = 0.61
- Sunflower seed = 0.59

Pasture-linked livestock commodities represented in the Singh dataset are attributed directly to pasture-related land-use change.

---

# Running the Notebook

Install requirements:

```bash
pip install pandas numpy matplotlib openpyxl
```

Run:

```bash
jupyter notebook trade_linked_livestock_LUC_analysis.ipynb
```

Then select:

```text
Run All
```

---

# Data Sources

### Singh et al. (2024)

https://zenodo.org/records/10633818

### FAOSTAT Supply Utilization Accounts

https://www.fao.org/faostat/en/#data/SCL

---

# License

### Code

MIT License.

### Data

Data remain subject to the licenses and terms of their respective providers.
