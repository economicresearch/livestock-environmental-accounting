
# Consumption-Based Terrestrial Animal-Product Greenhouse-Gas Emissions (2020–2022)

This workflow reproduces consumption-based greenhouse-gas emissions associated with terrestrial animal products for:

- Global North (GN)
- China (CN)
- Global South excluding China (GS)

using:

- EXIOBASE 3.9.6
- World Bank population statistics

The analysis is implemented in:

```text
exiobase_terrestrial_animal_product_CBA.ipynb
```

---

# Folder Structure

```text
exiobase/

├── exiobase_terrestrial_animal_product_CBA.ipynb
│
├── data/
│   ├── IOT_2020_ixi.zip
│   ├── IOT_2021_ixi.zip
│   ├── IOT_2022_ixi.zip
│   └── World_Bank_population.zip
│
├── outputs/
│
└── figures/
```

---

# Input Data

## 1. EXIOBASE 3.9.6

Official archive:

https://zenodo.org/records/15689391

Download:

- IOT_2020_ixi.zip
- IOT_2021_ixi.zip
- IOT_2022_ixi.zip

Place in:

```text
exiobase/data/
```

---

## 2. World Bank Population Data

Indicator:

```text
SP.POP.TOTL
```

Official portal:

https://data.worldbank.org/indicator/SP.POP.TOTL

Download the CSV archive and place it in:

```text
exiobase/data/
```

---

# Included Sectors

The analysis retains only:

- Meat products
- Dairy products
- Eggs

Excluded sectors:

- Fisheries
- Aquaculture
- Plant-based food sectors
- Non-food sectors

---

# Method Summary

The workflow applies environmentally extended multi-regional input-output accounting.

Emission intensities:

```text
f = F / x
```

Consumption-based emissions:

```text
E = f(I − A)^(-1)Y
```

where:

- A = technical coefficient matrix
- Y = final demand
- x = total output
- F = environmental extensions

Final demand includes:

- Household consumption
- Government consumption
- NPISH

Results are aggregated to:

- Global North
- China
- Global South excluding China

and normalized using World Bank population statistics.

---

# Running the Notebook

Install requirements:

```bash
pip install pandas numpy matplotlib openpyxl
```

Run:

```bash
jupyter notebook exiobase_terrestrial_animal_product_CBA.ipynb
```

Then select:

```text
Run All
```

---

# Data Sources

### EXIOBASE 3.9.6

https://zenodo.org/records/15689391

### World Development Indicators

https://data.worldbank.org/indicator/SP.POP.TOTL

---

# License

### Code

MIT License.

### Data

Data remain subject to the licenses and terms of their respective providers.
