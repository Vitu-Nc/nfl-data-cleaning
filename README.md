# NFL Play-by-Play: Data Cleaning and Power BI Dashboard

Dataset: NFL Play by Play 2009-2017 (Kaggle, maxhorowitz)

## Cleaning steps
1. Loaded 407,688 rows x 102 columns (27.67% of cells missing)
2. Found most missing values mean "does not apply" (e.g. RunGap on a pass play)
3. Filtered out game events (timeouts, quarter ends): -26,874 rows
4. Filled 5 rare-event text columns with "None"
5. Dropped rows with empty desc or posteam: -54 rows
6. Checked duplicates (0), converted Date to datetime
7. Left EPA, WPA and probability columns as NaN to avoid biasing averages
8. Trimmed to 42 columns for Power BI

## How to reproduce
Download the dataset from Kaggle into a Data/ folder, then run practice.ipynb.