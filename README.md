# World Bank GDP by Country & Continent (2000–2025)
A clean, visual, non-technical analysis of World Bank GDP (current US$) organized by country and summarized to a 7-continent view. All values are expressed in USD (billions) for readability.

---

## Why this repo exists
To provide a single place to:
- Extract authoritative GDP data from the World Bank (2000–2025),
- Publish & share a tidy dataset on Kaggle,
- Analyze & present insights in a visual, plain-English notebook.

---

## What’s included

- **Dataset (wide format)**: gdp_2000_2025.csv
  Columns: Name of country, Continent, 2000, 2001, …, 2025 (values in USD billions).
- **Notebook:** world-bank-gdp-by-country-continent.ipynb
  Visual, non-technical walkthrough covering leaders, continent shares, long-run deltas, COVID shock & recovery, pre/post-COVID growth, volatility, and global trendlines.

---

## Data source & extraction 
- **Source APIs:** World Bank Country metadata and GDP indicator NY.GDP.MKTP.CD (current US$), for years 2000–2025.
- **Process:** Pull countries and GDP values with pagination → clean names/regions → map countries to 7 continents
  (Oceania grouped under Australia for a business-friendly view) → convert to USD (billions) → export a single wide CSV.
- **Guardrail:** The analysis uses a “latest reliable year” concept (≥70% country coverage) to avoid biased “current” comparisons.
- **Note:** Antarctica has no countries; it will not appear in the dataset.

**Kaggle dataset:** https://www.kaggle.com/datasets/naveenapaleti/world-bank-gdp-by-country-and-continent20002025

---

## Notebook
- **Leaders & shares:** Top economies in the latest reliable year; continent pie; stacked area over time.
- **Winners since 2000:** Absolute GDP change (capped at ≤2024 for fairness).
- **COVID lens:** 2019→2020 shock distribution and years to recover to 2019 levels.
- **Growth regimes:** Pre- vs Post-COVID CAGR (who accelerated, who slowed).
- **Volatility radar:** Who’s steady vs lumpy (YoY variability).
- **Global line:** Total world GDP over time.

**Kaggle notebook:** https://www.kaggle.com/code/naveenapaleti/world-bank-gdp-by-country-continent

---

## Assumptions & design choices

- **Units:** Scaled to USD (billions); growth rates are scale-invariant.
- **“Latest reliable year” rule:** Year is “current” only if ≥70% of countries report data.
- **Fair comparisons:** Long-range deltas are capped at ≤2024 to avoid over-crediting countries missing the newest year.

---

## Update cadence
- World Bank GDP (indicator NY.GDP.MKTP.CD) updates annually.
- Recommended: Refresh this dataset once per year after the World Bank’s release.

---

## Licensing & attribution
- **Data:** © World Bank — CC BY 4.0 (attribution required).
- **Include:** “Contains World Bank Group data, used under CC BY 4.0. The World Bank does not endorse this work.”
- **Code & notebook:** MIT License.

---

## Contributing
Pull requests welcome. Please keep it dependency-light, preserve the USD (billions) convention, and document any taxonomy or methodology changes in the README.

---

## Contact
Feedback, issues, or feature requests (e.g., per-capita or PPP variants)? Open an issue on GitHub or use the repo’s discussions.
