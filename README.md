# Analyzing World Happiness

Exploring associations between country-level happiness scores, population health, and socioeconomic indicators using R.

## Overview
This collaborative project merges World Happiness Report 2021, World Data by Country 2020, and World Health Statistics data. The analysis includes country-name harmonization, missing-data assessment, CART imputation with MICE, regression, correlation analysis, and diagnostic visualizations.

The report's final regression includes meat consumption, premature mortality from cardiovascular disease/cancer/diabetes/chronic respiratory disease, and basic drinking-water access. These are observational associations, not evidence of causation. Reported overall model: F(3,139) = 107.3, p < 2.2e-16. Results are from the supplied report and have not been independently rerun.

## Files
- Analysis.Rmd — supplied analysis code, with machine-specific export paths replaced by relative paths.
- Report.pdf — original team report.
- Presentation.pdf — original team presentation.

## Team and attribution
Abhinaya Malempati, Adekola Adepoju, Daniel Adepoju, Daniel Cheruiyot, Noah Hamilton, Shivani Gaikwad.
The original R Markdown header credits Noah Hamilton and is preserved. No individual authorship of all code is claimed.

## Data availability and setup
The original Data folder is unavailable and is not included. The analysis cannot run end to end without reconstructing it from these sources:
- https://www.kaggle.com/datasets/ajaypalsinghlo/world-happiness-report-2021
- https://www.kaggle.com/datasets/daniboy370/world-data-by-country-2020
- https://www.kaggle.com/datasets/utkarshxy/who-worldhealth-statistics-2020-complete

Expected layout: Data/world-happiness-report-2021.csv, Data/WorldData/*.csv, and Data/WorldHealth/*.csv. Exact health filenames are declared in Analysis.Rmd. Review source licenses before redistributing datasets.

Open Analysis.Rmd in RStudio. Install packages required by its library calls before rendering; its original install block does not cover every dependency. PDF output requires a LaTeX installation. No package lockfile or full execution validation is available.

## Interpretation notes
MICE is configured with m = 1; this produces a single completed dataset, not pooled multiple-imputation inference. The code fits reduced regression formulas explicitly; the report describes backward selection, but an automated backward-selection routine is not present. Country-level findings should not be applied to individuals. Missingness, time-period differences, model selection, and cross-country dependence may affect the findings.
