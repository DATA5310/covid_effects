# Covid Effects on other Diseases

## Description

Briefly, compare the changes in incidence/prevalence of various diseases and other health metrics in the United States pre-covid and post-covid. Pre-covid is defined as pre-2020, as the first confirmed case of covid-19 in the U.S. was reported by the CDC on [January 20, 2020](https://www.cdc.gov/museum/timeline/covid19.html).

## Data Sources

| Description | Source | Data Year | Publication Year | Link | Additional Comments |
| ------------- | -------------- | -------------- | -------------- | -------------- | -------------- |
| Disability and Health Data System | CDC | 2022 | 2024 | https://data.cdc.gov/Disability-Health/Disability-and-Health-Data-System-DHDS-/k62p-6esq/about_data | | 
| Prevalence of Disability Status and Types | CDC | 2022 | 2024 | https://data.cdc.gov/Disability-Health/DHDS-Prevalence-of-Disability-Status-and-Types/s2qv-b27b/about_data | |
| Cancer Statistics  | CDC | 2021 | 2024 | https://www.cdc.gov/united-states-cancer-statistics/dataviz/data-tables.html | | 
| Chronic Disease Indicators | CDC | 2023 | 2023 | https://data.cdc.gov/Chronic-Disease-Indicators/U-S-Chronic-Disease-Indicators-CDI-2023-Release/g4ie-h725/about_data | The indicators are further described [here](https://www.cdc.gov/mmwr/preview/mmwrhtml/rr6401a1.htm) |
| Alzheimer's Disease and Healthy Aging Data | CDC | 2022 | 2024 | https://data.cdc.gov/Healthy-Aging/Alzheimer-s-Disease-and-Healthy-Aging-Data/hfr9-rurv/about_data | |
| Underlying Cause of Deaths | CDC | 2022 | 2024 | https://wonder.cdc.gov/controller/datarequest/D158 | Dataset description [here](https://wonder.cdc.gov/wonder/help/ucd-expanded.html#). List of ICD-10 codes [here](https://www.icd10data.com/ICD10CM/Codes) |
| Chronic Health Indicators | BRFSS | 2023 | 2024 | https://data.cdc.gov/Behavioral-Risk-Factors/BRFSS-Table-of-Chronic-Health-Indicators/u7k3-tu8b | This is the source for some of the data in CDI. This has 2 more years of data. |
| US: Daily COVID-19 vaccine doses administered | Our World in Data / CDC | 2023 | 2024 | https://ourworldindata.org/grapher/us-daily-covid-vaccine-doses-administered?tab=table&time=2021-06-05..latest#sources-and-processing | |
| Deaths involving Coronavirus Disease | U.S. DHHS | 2023 | 2023 | https://catalog.data.gov/dataset/conditions-contributing-to-deaths-involving-coronavirus-disease-2019-covid-19-by-age-group | |

Read the above as: The 'Cancer Statistics' dataset was published in 2024 and contains data from 2021 and earlier.

## Quick Start

1. Make sure Anaconda / Miniconda is installed.
- **Mac**:
    ```
    brew install --cask miniconda
    ```

2. Then create a new environment:

```
conda create -n covid_effects -c conda-forge python=3.11 numpy pandas gitpython ipykernel chardet matplotlib seaborn scikit-learn pytorch u8darts-all prophet plotly ipywidgets nbconvert
```

3. Activate environment:

```
conda activate covid_effects
```

4. To compile the presentation notebook:

```
jupyter dejavu 2.presentation.ipynb --to slides --SlidesExporter.reveal_theme=simple
```

In the browser, make sure to add the params to configure reveal.js -- mainly the auto-animation speed `...2.presentation.slides.html?autoAnimateDuration=0.8`

While developing, this is the one-liner used to make it easier

```
jupyter dejavu 2.presentation.ipynb --to slides --SlidesExporter.reveal_theme=simple && osascript -e 'tell application "Safari" to open location "file://'$(pwd)'/2.presentation.slides.html?autoAnimateDuration=0.8&scrollProgress:false"'
```

5. Now you should be able to run any notebooks in this repo.


