# The Price of a Pretty Face

This STAT 330 project examines the relationship between perceived attractiveness and annual income. Its central question is whether attractiveness is associated with income after accounting for height, cognitive ability, sex, BMI, and waist circumference.
## Repository contents

- `Proposal_Template_FINISHED.qmd` — Quarto source for the proposal and preliminary analysis.
- `Proposal_Template_FINISHED.html` — an existing rendered copy of the proposal. Re-render the QMD to refresh this file after source changes.
- `data.csv` — the analysis subset, with columns for `height`, `looks`, `iq`, `income`, `sex`, `bmi`, and `waist`.
- `portfolio/` — Quarto website files for the case study and AI-use record. The pages are still assignment templates with prompts and placeholders.

## Data and privacy

The analysis uses data from the Wisconsin Longitudinal Study (WLS), which follows Wisconsin high school graduates from 1957. The proposal identifies annual income as the response and perceived attractiveness, height, and cognitive ability as key predictors. The current model also includes sex, BMI, and waist circumference.

Consult the [WLS documentation](https://researchers.wls.wisc.edu/documentation/) for study details and data access terms. Protect participant confidentiality, do not attempt to identify participants, and do not upload participant-level WLS data to external AI services.

## Requirements

- [Quarto](https://quarto.org/docs/get-started/)
- R
- R packages: `tidyverse` and `haven`

Install the R packages in an R console:

```r
install.packages(c("tidyverse", "haven"))
```

## Render and preview

Render the proposal from the repository root:

```sh
quarto render Proposal_Template_FINISHED.qmd
```

Preview the portfolio site:

```sh
cd portfolio
quarto preview
```

## Current project status

The proposal reads `data.csv` and fits a preliminary linear model using all six listed predictors. The exploratory plotting code still refers to `my_subset`, which is not defined in the current QMD (the loaded data frame is `my_data`), so fix those references before rendering. The tracked HTML may also be out of date relative to the QMD. The portfolio site remains a template and needs its prompts replaced with the completed analysis.

Attractiveness ratings are subjective, and the study represents a specific historical cohort. These limits should be considered when interpreting results or generalizing them to other populations.

## Authors

Bradley Swalberg, Henri Ly, and Heidi Turley.
