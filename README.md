# NHS Emergency Admissions Analysis

This project analyses ten years of NHS Hospital Episode Statistics diagnosis data to identify the most and least frequent causes of emergency admissions.

## Research Question

What are the most and least frequent emergency admissions over the last 10 years?

## Project Overview

The project processes annual NHS admitted patient care diagnosis workbooks from 2012-13 to 2021-22. The analysis combines yearly diagnosis-level data, extracts emergency admission counts, and compares diagnosis frequencies across the ten-year period.

The current combined dataset focuses on:

- diagnosis code
- diagnosis description
- emergency admission count
- year

## Key Findings

Based on the combined diagnosis-level dataset, the most frequent emergency admission diagnosis groups over the ten-year period include:

| Rank | Code | Diagnosis | Total emergency admissions |
| --- | --- | --- | ---: |
| 1 | R07 | Pain in throat and chest | 2,384,874 |
| 2 | R10 | Abdominal and pelvic pain | 2,261,379 |
| 3 | J18 | Pneumonia, organism unspecified | 2,095,314 |
| 4 | N39 | Other disorders of urinary system | 1,380,278 |
| 5 | J44 | Other chronic obstructive pulmonary disease | 1,143,376 |

The least frequent diagnosis groups are rare conditions or residual/sequelae categories, with several diagnosis groups recording only one emergency admission across the combined period.

Annual emergency admissions increased from 5,336,043 in 2012-13 to 6,509,586 in 2019-20, decreased to 5,450,837 in 2020-21, then rose again to 6,210,641 in 2021-22.

## Files

- `DataAnalysis.ipynb` - main notebook for data preparation and analysis
- `total.ipynb` - additional analysis notebook
- `extract_all_fields.ipynb` - batch extraction notebook that keeps all available primary diagnosis fields across ten years
- `hospital_diagnosis_combined.xlsx` - combined processed dataset
- `hospital_diagnosis_all_fields.xlsx` - expanded combined dataset with one `AllFields` sheet containing all available diagnosis-level fields
- `data/` - original annual NHS diagnosis workbooks
- `workshop 1.twb` - Tableau workbook for visualisation

## Possible Extensions

The current analysis answers the main frequency question, but the project can be made more analytical by studying how emergency admissions changed over time and across patient groups.

Recommended extensions:

1. Trend analysis by diagnosis
   - Track the yearly emergency admission count for the top diagnosis groups.
   - Calculate absolute change and percentage change between 2012-13 and 2021-22.
   - Identify diagnoses with the largest increases and decreases.

2. Age-group analysis
   - Use the age columns in the original NHS files, such as `Mean age`, `Age 0`, `Age 1-4`, ..., `Age 90+`.
   - Compare whether different diagnosis groups are concentrated in children, working-age adults, or older patients.
   - Group ages into broader categories such as `0-14`, `15-44`, `45-64`, `65-84`, and `85+`.

3. Sex-based comparison
   - Use the `Male`, `Female`, and `Gender Unknown` columns from the original files.
   - Compare whether high-frequency emergency admissions differ by sex.
   - Calculate male-to-female ratios for major diagnosis groups.

4. Pre- and post-2020 comparison
   - Compare patterns before and after 2020-21, since emergency admission volumes changed sharply during the COVID-19 period.
   - Examine respiratory conditions, infections, and emergency-use diagnosis codes separately.

5. Normalised ranking
   - Compare each diagnosis as a percentage of all emergency admissions in that year.
   - This helps distinguish real changes in diagnostic patterns from changes in total hospital activity.

6. Visualisation
   - Add line charts for ten-year trends.
   - Add stacked bar charts by age group or sex.
   - Add a heatmap showing diagnosis categories by year.

## Suggested Method

For a stronger research-methods submission, the analysis could follow this structure:

1. Clean and combine the yearly diagnosis data.
2. Rank diagnosis groups by total emergency admissions.
3. Analyse yearly trends for the top diagnosis groups.
4. Compare changes across age groups and sex where fields are available.
5. Discuss possible explanations, including demographic change, coding changes, seasonal disease patterns, and the COVID-19 period.

## Data Source

The project uses NHS Hospital Episode Statistics admitted patient care diagnosis workbooks for England.
