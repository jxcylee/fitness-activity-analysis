# Fitness Activity Statistical Analysis (R)

A statistics course project analyzing 45 days of smartwatch activity data using R. The analysis examines daily step counts, active minutes, weekday/weekend patterns, step-goal attainment, and changes across three periods of a semester.

## Project overview

The project uses descriptive statistics and inferential methods to investigate six questions:

1. Does the average daily step count exceed the 8,500-step benchmark used in the assignment?
2. Does average daily step count differ between weekdays and weekends?
3. Do the data meet the conditions for a one-proportion z-test of the claim that the 10,000-step goal is reached on more than 90% of days?
4. Is meeting the 10,000-step goal associated with day type?
5. Is mean daily step count different across the three semester phases?
6. How strongly are daily step count and active minutes linearly associated?

## Methods and tools

- **Language:** R
- **Authoring/report format:** Quarto (`.qmd`)
- **Descriptive analysis:** mean, median, standard deviation, variance, five-number summary, histograms, and boxplots
- **Inference:** one-sample z-test, Welch two-sample t-test, chi-square test of independence, and one-way ANOVA
- **Regression:** simple linear regression, correlation, confidence intervals, and model fit

The analysis uses base R and functions from R's standard `stats` package.

## Selected results

- Mean daily steps: **8,886** (45 observations)
- Mean daily active minutes: **71.02** (45 observations)
- Weekday mean: **9,330.55 steps**; weekend mean: **7,663.50 steps**
- Weekday/weekend Welch test: **t = 2.5644**, **p = 0.0216**
- Chi-square test of day type and step-goal attainment: **p = 0.4666**
- One-way ANOVA across the three phases: **F = 2.7864**, **p = 0.0731**
- Steps/active-minutes regression: **R² = 0.9995**

These results describe this 45-day dataset and should not be generalized beyond its scope without additional data and appropriate sampling assumptions.

## Repository contents

```text
fitness-activity-analysis/
├── README.md
├── analysis.qmd
├── project.Rproj
└── report/
    └── final-report.pdf
```

- `analysis.qmd` contains the R code, data vectors, analysis, and written discussion.
- `report/final-report.pdf` is the rendered 18-page report.
- `project.Rproj` is the RStudio project file.

## Reproducing the report

1. Open `project.Rproj` in RStudio (or open the folder as an RStudio project).
2. Make sure [Quarto](https://quarto.org/) is installed and available to RStudio.
3. Open `analysis.qmd` and render it to PDF.

The observations are currently stored as vectors in the Quarto source file; there is no separate data file.

## Scope and limitations

- The dataset contains 45 days of activity observations for one individual.
- The project uses the benchmark and hypotheses specified for the course assignment.
- The one-proportion z-test was not carried out because the expected number of failures under the stated null proportion was below 5.
- A non-significant result is not proof that groups or variables are identical or independent; it indicates insufficient evidence against the relevant null hypothesis at the selected significance level.
- The very high steps/active-minutes regression fit should be interpreted cautiously. The active-minute values closely track a near-proportional function of step count in this dataset, so the relationship should not be presented as evidence of causation.

## Academic context

This project was completed for MATH 1320: Introduction to Probability and Statistics. The dataset was supplied by the course instructor for the project.
