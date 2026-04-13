# District-Level Social Deprivation Analysis — India (NFHS-5)

A portfolio project analysing multidimensional deprivation across 707 Indian 
districts using National Family Health Survey data (NFHS-5, 2019-21).

## Project Overview

This project constructs a **Composite Deprivation Index** for every district 
in India across three dimensions — Health, Education, and Living Standards — 
using 13 indicators drawn from NFHS-5 district factsheets. The methodology 
follows the Alkire-Foster framework used by NITI Aayog's National MPI.

## Key Findings

- Health is the most deprived dimension nationally (avg score: 43.2/100)
- Education is the strongest predictor of overall deprivation (r = 0.68)
- Bihar and Tripura are the most deprived states; Kerala the least
- Gujarat ranks among the most deprived despite high GDP — illustrating 
  the limits of economic growth as a development measure
- Mewat (Haryana) is the most extreme district-level outlier in India, 
  scoring 17.6 points above its state average
- Health deprivation is structurally independent of living standards and 
  education (r = -0.19, -0.20), pointing to failures in nutrition and 
  primary healthcare delivery


## Methodology

| Step | Description |
|---|---|
| Indicator selection | 13 indicators across 3 dimensions |
| Direction alignment | "Higher = better" indicators flipped via 100 - x |
| Dimension scores | Simple average within each dimension |
| Composite index | Equal-weighted average of 3 dimension scores |
| Missing values | 13 districts with unreliable estimates (*) imputed using state mean |

## Tools and Packages

- **R** with RStudio
- `readxl` — data import
- `dplyr`, `tidyr` — data manipulation
- `ggplot2` — visualisation
- `janitor`, `skimr` — data cleaning and exploration
- `rmarkdown` — policy brief generation

