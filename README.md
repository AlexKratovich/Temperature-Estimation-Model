# Temperature Estimation Model

A collaborative University of Washington machine-learning project by **Bryan Zhang and Alexey Kratovich**. The original report credits Bryan Zhang and Alex Kratovich; those credits and its source acknowledgments are retained.

**[View the project report](https://AlexKratovich.github.io/Temperature-Estimation-Model/)**

## Project

Estimate Seattle (KBFI) temperature from simultaneous observations at three nearby airport stations: Everett (KPAE), Bremerton (KPWT), and Tacoma (KTIW).

- Scraped historical weather tables for four stations across 31 days using Selenium and BeautifulSoup.
- Cleaned station data with Pandas, resampled to 30-minute intervals, and interpolated missing values.
- Compared linear regression and decision-tree regression using an 80/20 random train/test split.

| Model | Reported test R² |
| --- | ---: |
| Linear regression | 0.9621 |
| Decision tree | 0.9705 |

These are the results recorded in the original report, not newly rerun experiments. R² measures regression fit; it is not a percentage accuracy score.

## Authors

- **Alexey Kratovich** ([AlexKratovich](https://github.com/AlexKratovich)): data cleaning and collaborative resampling, interpolation, modeling, and evaluation.
- **Bryan Zhang**: project partner and coauthor.

## Contents

`index.html` is the static notebook report, including Python code, a sample data table, explanations, source acknowledgments, and two embedded evaluation plots. Open it in a browser or use the hosted report link. Unused notebook-template scripts and references to missing local JavaScript assets were removed for standalone hosting; the report's project content was retained.

The original notebook and scraped CSV files are not included in the supplied HTML export, so this repository provides a readable report rather than a complete reproducible training environment.

## Evaluation limits

The model estimates temperature from known readings at the same time; it does not forecast future weather. Evaluation used a random split of a single month, with no chronological holdout or additional evaluation. The original export also contains a date inconsistency: scraping URLs and narrative refer to January 2024, while preprocessing assigns January 2025 timestamps. The report is preserved rather than silently correcting this discrepancy.
