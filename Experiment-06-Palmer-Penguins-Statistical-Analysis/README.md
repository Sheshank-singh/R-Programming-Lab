# Experiment 06 — Statistical Analysis of Physical Characteristics of Palmer Penguins

## Domain

Statistical Data Analysis

## Objective

The objective of this experiment is to perform statistical analysis of the physical characteristics of Palmer Penguins using R.

The analysis focuses on body mass and flipper length across the three penguin species:

- Adelie
- Chinstrap
- Gentoo

Descriptive statistics, hypothesis testing, effect size analysis, ANOVA, non-parametric testing, and visualization techniques are applied to understand differences between species and sexes.

## Dataset

**Palmer Penguins Dataset**

The dataset contains physical and categorical information about penguins, including:

- Species
- Island
- Bill Length
- Bill Depth
- Flipper Length
- Body Mass
- Sex

The dataset contains **344 penguin observations** across three species.

## Tasks Performed

### Task 1 — Descriptive Statistical Analysis

Descriptive statistics were calculated for `body_mass_g`, including:

- Mean
- Median
- Minimum and Maximum
- Variance
- Standard Deviation
- First Quartile (Q1)
- Third Quartile (Q3)
- Interquartile Range (IQR)
- Skewness
- Kurtosis

Descriptive statistics were also calculated separately for each penguin species.

Visualizations include:

- Histogram
- Boxplot
- Density plot

### Task 2 — Male vs Female Body Mass Analysis

Male and female penguin body masses were compared using statistical hypothesis testing.

The analysis includes:

- Null and alternative hypotheses
- Shapiro-Wilk normality test
- Q-Q plots
- Independent two-sample t-test
- 95% confidence interval
- Cohen's d effect size
- Interpretation of statistical significance and effect size

### Task 3 — One-Way ANOVA

A one-way ANOVA was performed to examine whether mean body mass differs significantly among penguin species.

The analysis includes:

- Normality assessment
- Levene's test for homogeneity of variance
- One-way ANOVA
- F-statistic
- Degrees of freedom
- p-value
- Tukey HSD post-hoc test

Pairwise differences between:

- Adelie vs Chinstrap
- Adelie vs Gentoo
- Chinstrap vs Gentoo

were evaluated using Tukey's HSD test.

### Task 4 — Kruskal-Wallis Test

Because some ANOVA assumptions were substantially violated, a non-parametric Kruskal-Wallis test was performed as an additional analysis.

The results were compared with the one-way ANOVA conclusions to determine whether the overall species differences remained statistically significant.

### Task 5 — Two-Way ANOVA

A two-way ANOVA was performed using:

`body_mass_g ~ species * sex`

The analysis evaluates:

- Main effect of species
- Main effect of sex
- Species × sex interaction

The interaction effect was examined to determine whether the relationship between sex and body mass differs across penguin species.

### Task 6 — Flipper Length Analysis

The statistical analysis was repeated for `flipper_length_mm` to examine differences in flipper length among penguin species.

The analysis includes:

- Species-wise descriptive statistics
- Normality testing
- Levene's test
- One-way ANOVA
- Tukey HSD post-hoc test
- Kruskal-Wallis test

### Task 7 — Visualization and Interpretation

The following visualizations were created:

- Body mass histogram
- Species-wise body mass boxplot
- Sex-wise body mass boxplot
- Q-Q plots
- Species-wise flipper length comparison
- Group comparison plots

The visualizations were used to support the statistical findings and interpretation.

## Technologies

- R
- Google Colab
- dplyr
- tidyr
- ggplot2
- moments
- Palmer Penguins Dataset
- Statistical Hypothesis Testing
- ANOVA
- Tukey HSD
- Kruskal-Wallis Test

## Deliverables

- R source code
- Google Colab notebook
- PDF report
- Statistical analysis results
- Data visualizations
- Interpretation and conclusions

## Key Statistical Findings

The analysis shows substantial differences in **body mass among penguin species**, with Gentoo penguins having considerably higher body mass than Adelie and Chinstrap penguins.

The male and female body mass comparison also indicates a statistically significant difference, with a **large effect size**.

For flipper length, statistically significant differences were observed among all three penguin species, with Gentoo penguins having the longest flippers on average.

Both parametric and non-parametric analyses provide strong evidence of species-level differences in the physical characteristics examined.
