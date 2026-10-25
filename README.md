# World Economic Outlook 2026 | IMF Data Analysis

## Project Overview

This project explores global economic trends using the **International Monetary Fund (IMF) World Economic Outlook (WEO), October 2026** dataset. The goal is to use Python to examine economic performance, compare countries and regions, and turn complex economic indicators into clear visual insights.

The IMF's October 2026 report, *Resilience Under Strain, Urgent Choices*, describes a global economy that remains resilient but faces uneven growth and rising risks. Geopolitical conflicts, higher energy and food prices, trade tensions, and limited fiscal flexibility create challenges. Meanwhile, investment in artificial intelligence (AI) and technology supports activity in some economies, although its benefits are not evenly shared.

## Key IMF Findings

| Indicator | 2026 forecast | 2027 forecast |
| --- | ---: | ---: |
| Global economic growth | 3.1% | 3.4% |
| Global headline inflation | 4.7% | 4.1% |

The forecasts indicate that growth continues despite uncertainty, while inflation remains an important concern. These figures are **IMF projections**, not final observed outcomes.

## Data Source

- **Publisher:** International Monetary Fund (IMF)
- **Dataset:** World Economic Outlook (WEO), October 2026
- **Frequency:** Annual
- **Coverage:** Historical observations from 1980 onward, with forecasts for most series extending approximately five years ahead. Some countries and indicators have missing values.
- **Excel workbook sheets:** `Countries`, `Country Groups`, and `Commodity Prices`

**Links:**

- [IMF World Economic Outlook Data Portal](https://data.imf.org/datasets/WEO)
- [October 2026 WEO Excel Dataset](https://data.imf.org/-/media/iData/External-Storage/Documents/0FA3DC49A04D446E9D69DBEB29979E1C/en/WEOOct2026all.xlsx)
- [October 2026 WEO Report](https://www.imf.org/en/Publications/WEO/Issues/2026/10/13/world-economic-outlook-october-2026)

The WEO provides indicators such as GDP, inflation, unemployment, government finances, external balances, and international trade.

## Project Objectives

1. Examine economic growth and inflation over time.
2. Compare economic performance among selected countries and regions.
3. Explore relationships between GDP growth, inflation, and unemployment.
4. Identify differences between historical results and IMF projections.
5. Create clear charts and summaries that explain economic trends.

## Research Questions

1. Which countries have the highest and lowest projected GDP growth in 2026 and 2027?
2. How do inflation forecasts differ across countries and regions?
3. How has unemployment changed across selected economies?
4. Is there an observable relationship between inflation and GDP growth?
5. Which economies are forecast to improve or slow down between 2026 and 2027?

## Tools and Libraries

- **Python** — data analysis
- **Pandas** — loading, cleaning, and transforming data
- **NumPy** — numerical operations
- **Matplotlib and Seaborn** — data visualisation
- **Jupyter Notebook** — reproducible analysis
- **OpenPyXL** — reading Excel files

## Getting Started

1. Download the Excel workbook using the link above and place it in a folder named `data`.
2. Install the packages:

   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl jupyterlab
   ```

3. Launch JupyterLab with `jupyter lab`, or use a Python notebook in VS Code.
4. Inspect the workbook sheets before selecting columns and cleaning data:

   ```python
   import pandas as pd

   file_path = "data/WEOOct2026all.xlsx"
   workbook = pd.ExcelFile(file_path)
   print(workbook.sheet_names)

   # Inspect the raw layout before choosing the appropriate header rows.
   preview = pd.read_excel(file_path, sheet_name="Countries", header=None, nrows=10)
   print(preview.to_string(index=False, header=False))
   ```

   **Note:** The workbook may contain introductory or metadata rows. Identify the correct header row and indicator definitions before performing analysis.

## Suggested Visualisations

- **Line chart:** GDP growth trends and forecasts for selected countries.
- **Bar chart:** Top and bottom countries by forecast GDP growth in 2026.
- **Heatmap:** Inflation rates across countries and years.
- **Scatter plot:** Inflation versus GDP growth for a selected year.

## Data Quality and Interpretation

- Distinguish **actual figures, estimates, and forecasts**. Forecasts may change in future IMF releases.
- Check missing values, country classifications, indicator units, and definitions before comparisons.
- Do not mix country-level figures with regional aggregates in country rankings.
- Avoid comparing nominal GDP with GDP growth rates or purchasing-power-parity measures without clear labels.
- Correlation does not establish causation; for example, AI investment cannot be isolated as the cause of growth using only these charts.
- Record the **October 2026 dataset vintage** so the analysis can be reproduced even after the IMF publishes newer forecasts.

## Expected Outcomes

The project will produce a cleaned dataset, reproducible Python analysis, country and regional comparisons, and charts highlighting important economic patterns. The findings can help readers understand how global shocks, inflation, and technological change coincide with different growth trajectories.

## Acknowledgement

Data and economic forecasts are provided by the **International Monetary Fund (IMF)**. Interpretations, analysis, and visualisations produced in this repository are those of the project author and do not represent official IMF conclusions.

**Source:** IMF, *World Economic Outlook*, October 2026.
