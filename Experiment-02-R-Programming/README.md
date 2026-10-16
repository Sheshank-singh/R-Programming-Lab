# Experiment 02 — R Programming: Data Cleaning and Missing Data Handling

## Domain

R Programming, Data Cleaning, and Data Preprocessing

## Objective

The objective of this experiment is to apply control flow, custom functions, error handling, loops, vectorized operations, and missing-data treatment techniques in R.

The experiment consists of two practicals:

- **Lab 3 — Control Flow for Data Cleaning:** Clean invalid resting blood pressure values, handle errors safely, compare loop-based and vectorized operations, and validate the cleaned data.
- **Lab 4 — Advanced Missing Data Handling:** Identify different forms of missing and invalid data, apply suitable treatment strategies, perform median imputation, visualize missingness, and validate the processed dataset.

## Dataset

### Lab 3 — UCI Heart Disease Dataset

The UCI Heart Disease dataset contains patient-related clinical variables used for cardiovascular analysis.

Relevant attributes include:

- Age
- Sex
- Resting Blood Pressure (`trestbps`)
- Serum Cholesterol (`chol`)
- Maximum Heart Rate (`thalach`)
- Chest Pain Type (`cp`)
- Number of Major Vessels (`ca`)
- Heart Disease Diagnosis (`num`)

The analysis focuses on resting blood pressure. Negative values, missing values, and extreme readings are deliberately introduced to simulate data-entry problems.

### Lab 4 — UCI Adult / Census Income Dataset

The UCI Adult dataset contains demographic and employment-related information.

Relevant attributes include:

- Age
- Work Class
- Final Weight (`fnlwgt`)
- Education
- Marital Status
- Occupation
- Relationship
- Race
- Sex
- Capital Gain
- Capital Loss
- Hours Worked per Week
- Native Country
- Income Category

The dataset is used to demonstrate missing-value detection, invalid-value handling, categorical treatment, and numerical imputation.

## Tasks Performed

### Lab 3 — Control Flow for Data Cleaning

#### Task 1 — BP-Cleaning Function

A custom function was developed using `if-else` statements to clean resting blood pressure values.

The function performs the following operations:

- Converts negative blood pressure values to `NA`.
- Caps values greater than 250 mmHg at 250.
- Retains valid blood pressure values without modification.
- Preserves missing values.

#### Task 2 — Error Handling Using `tryCatch()`

Error handling was implemented using `tryCatch()` to prevent invalid calculations from terminating the program.

The analysis includes:

- Calculating mean blood pressure when missing values are present.
- Calculating the ratio `chol / trestbps`.
- Handling zero, missing, negative, and invalid denominators.
- Displaying informative error or warning messages.

#### Task 3 — Loop-Based and Vectorized Cleaning

Two approaches were implemented to clean blood pressure values.

The analysis includes:

- Identifying invalid and extreme values using a `for` loop.
- Applying equivalent cleaning rules using vectorized R operations.
- Measuring execution time using `system.time()`.
- Comparing the outputs of both methods.
- Evaluating their computational performance.

#### Task 4 — Validation of Cleaned Blood Pressure Data

The cleaned dataset was validated using descriptive statistics and condition checks.

The validation includes:

- Counting missing blood pressure values.
- Calculating minimum and maximum blood pressure.
- Calculating mean and median blood pressure.
- Checking for remaining negative values.
- Checking for values greater than 250 mmHg.

#### Task 5 — Output Generation

The Lab 3 outputs include:

- `cleaned_heart_data.csv`
- `loop_vs_vectorized_timing.csv`
- `bp_validation_summary.csv`
- `lab3_conclusion.txt`

### Lab 4 — Advanced Missing Data Handling

#### Task 1 — Identification of Missing and Invalid Data

Different forms of missing and invalid data were examined using R.

The analysis includes:

- Identifying missing values using `is.na()`.
- Identifying `NaN` values using `is.nan()`.
- Demonstrating `NULL` using `is.null()`.
- Identifying blank strings using `x == ""`.
- Detecting impossible age values such as `age = 999`.
- Generating variable-wise missing-value summaries using `naniar::miss_var_summary()`.

The experiment also demonstrates that `NULL` represents the absence of an R object or value and is different from `NA`, `NaN`, and blank strings.

#### Task 2 — Missing-Data Treatment

Appropriate data-cleaning strategies were applied to the dataset.

The treatment includes:

- Converting impossible age values to `NA`.
- Replacing blank categorical values with `"Unknown"`.
- Identifying and removing observations containing `NaN` values where appropriate.
- Imputing missing numeric values using the median.
- Identifying complete and incomplete observations using `complete.cases()`.

#### Task 3 — Custom Median-Imputation Function

A reusable function was developed to impute missing values in numeric vectors.

The function performs the following operations:

- Accepts a numeric vector.
- Identifies missing observations.
- Calculates the median of valid observations.
- Replaces missing values with the median.
- Returns the processed vector.

#### Task 4 — Missingness Analysis and Visualization

Missingness was examined before and after data treatment.

The analysis includes:

- Calculating the number of missing values.
- Calculating the percentage of missing values.
- Generating variable-wise missingness summaries.
- Visualizing missingness patterns using `naniar::vis_miss()`.
- Comparing missingness before and after treatment.

#### Task 5 — Validation of the Cleaned Dataset

The cleaned dataset was examined using `skimr::skim()` and additional validation checks.

The validation includes:

- Checking for remaining impossible age values.
- Verifying that blank categorical values have been replaced.
- Checking selected numeric variables for untreated missing values.
- Reviewing the structure and summary statistics of the processed dataset.

#### Task 6 — Output Generation

The Lab 4 outputs include:

- `cleaned_adult_data.csv`
- `adult_missing_summary_before.csv`
- `adult_missing_summary_after.csv`
- `adult_missingness_comparison.csv`
- `adult_validation_results.csv`
- `lab4_conclusion.txt`

## Technologies

- R Programming
- Google Colab
- UCI Heart Disease Dataset
- UCI Adult / Census Income Dataset
- `tryCatch()`
- Conditional Statements and Loops
- Vectorized Operations
- `system.time()`
- `naniar`
- `skimr`
- Median Imputation
- Missing-Data Visualization
- Git and GitHub

## Deliverables

- Complete R source code
- Google Colab notebook
- PDF export of the executed notebook
- Custom BP-cleaning function
- Error-handling function using `tryCatch()`
- Loop and vectorized execution-time comparison
- Cleaned Heart Disease dataset
- Cleaned Adult dataset
- Before-and-after missingness summaries
- Missingness visualizations
- Validation results
- Conclusion and interpretation
- GitHub repository link

## Key Findings

The experiment demonstrates how R programming techniques can be used to address common data-quality problems in healthcare and demographic datasets.

In Lab 3, conditional statements and custom functions provide reusable rules for cleaning invalid blood pressure values. The comparison between loop-based and vectorized operations illustrates two approaches to data processing, while `tryCatch()` helps handle invalid calculations safely.

In Lab 4, the distinction between `NA`, `NULL`, `NaN`, and blank strings supports more accurate missing-data detection. Median imputation, categorical-value replacement, missingness visualization, and validation checks help prepare the dataset for further analysis.

The execution-time comparison and before-and-after missingness summaries should be interpreted using the actual results generated by running the notebook.

## Conclusion

This experiment provides practical experience in R-based data cleaning, control flow, custom function development, error handling, performance comparison, missing-data treatment, and data validation.

The two practicals demonstrate the importance of identifying invalid observations, applying suitable cleaning strategies, and verifying data quality before conducting statistical analysis or developing predictive models.
