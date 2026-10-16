# Experiment 04 — R Project Implementation and Vehicle Data Analysis

## Domain

R Programming, Exploratory Data Analysis, and Predictive Modelling

## Objective

The objective of this experiment is to perform data analysis and predictive modelling using R.

The analysis uses the `mtcars` dataset to investigate the relationship between vehicle characteristics and fuel economy (`mpg`).

Data inspection, cleaning, descriptive statistics, correlation analysis, visualization, and multiple linear regression are used to study the relationship between vehicle weight, horsepower, displacement, cylinder count, and fuel economy.

## Dataset

**Motor Trend Car Road Tests (`mtcars`) Dataset**

The dataset is available as a built-in dataset in R and contains information about different car models.

The dataset includes:

- Miles Per Gallon (`mpg`)
- Number of Cylinders (`cyl`)
- Displacement (`disp`)
- Gross Horsepower (`hp`)
- Rear Axle Ratio (`drat`)
- Vehicle Weight (`wt`)
- Quarter-Mile Time (`qsec`)
- Transmission Type (`am`)
- Number of Gears (`gear`)
- Number of Carburetors (`carb`)

The original dataset contains **32 observations and 11 variables**. The notebook adds a `car_name` column using the original row names and removes the row names.

## Tasks Performed

### Task 1 — Data Loading and Inspection

The built-in `mtcars` dataset was loaded into R for analysis.

The analysis includes:

- Loading the dataset using `data("mtcars")`
- Extracting vehicle names from row names
- Examining the number of rows and columns
- Inspecting the dataset structure using `str()`
- Displaying the first few observations using `head()`
- Calculating descriptive statistics using `summary()`
- Checking missing values for each variable

### Task 2 — Data Cleaning and Feature Preparation

The dataset was checked and prepared before performing the analysis.

The data preparation includes:

- Identifying and removing duplicate rows
- Validating positive values for `mpg`, `wt`, and `cyl`
- Checking that `hp` is non-negative
- Creating readable transmission labels from the `am` variable
- Representing transmission type as a factor with two categories:
  - Automatic
  - Manual

The number of rows before and after cleaning was also examined.

### Task 3 — Exploratory Data Analysis

Exploratory data analysis was performed to understand fuel economy and its relationship with vehicle characteristics.

The analysis includes:

- Calculating the number of observations by transmission type
- Computing mean and median fuel economy for each transmission type
- Calculating standard deviation for each transmission group
- Generating a correlation matrix for `mpg`, `cyl`, `disp`, `hp`, and `wt`
- Examining relationships between vehicle characteristics and fuel economy

### Task 4 — Data Visualization

The following visualizations were created using `ggplot2`:

- **Vehicle Weight and Fuel Economy:** A scatter plot showing the relationship between vehicle weight and `mpg`, grouped by transmission type, with fitted linear trend lines.
- **Fuel Economy by Transmission Type:** A boxplot comparing fuel economy between automatic and manual transmission vehicles.
- **Fuel Economy by Number of Cylinders:** A boxplot comparing fuel economy across vehicles with different cylinder counts.
- **Actual vs Fitted Fuel Economy:** A scatter plot comparing observed fuel economy with values estimated by the regression model, including a reference line.

These visualizations help examine trends, group differences, and the agreement between actual and fitted fuel economy.

### Task 5 — Predictive Analysis Using Linear Regression

A multiple linear regression model was developed using the `lm()` function in R.

The model uses the following formula:

`mpg ~ wt + hp + disp + cyl`

The response variable is `mpg`, while the predictor variables are:

- Vehicle weight (`wt`)
- Horsepower (`hp`)
- Displacement (`disp`)
- Number of cylinders (`cyl`)

The analysis includes:

- Fitting the multiple linear regression model
- Examining model coefficients and the model summary
- Generating fitted fuel economy values
- Calculating residuals as the difference between actual and fitted values
- Comparing actual and fitted fuel economy

### Task 6 — Regression Model Evaluation

The fitted model was evaluated using the following metrics:

- **Root Mean Squared Error (RMSE):** Measures the typical magnitude of prediction errors while penalizing larger errors.
- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and fitted values.
- **R-squared:** Measures the proportion of variation in fuel economy explained by the fitted model.

The metrics were calculated using predictions on the same observations used to fit the model. Therefore, they represent **in-sample performance** rather than performance on an independent test dataset.

### Task 7 — Result Validation and Output Generation

The notebook includes sections for validating the analysis and saving project outputs.

The intended project outputs are:

- Vehicle analysis data in CSV format
- Regression evaluation metrics in CSV format
- Regression model summary in text format

The outputs are intended to be organized inside an `outputs` directory for easier access and project management.

The final output files should be verified after executing the corresponding notebook cells.

## Technologies

- R Programming
- R version 4.6.1
- ggplot2 version 4.0.3
- `mtcars` Dataset
- Exploratory Data Analysis
- Descriptive Statistics
- Correlation Analysis
- Data Visualization
- Multiple Linear Regression
- RMSE, MAE, and R-squared
- Git and GitHub

## Deliverables

- Google Colab notebook (`Lab_Problem_04.ipynb`, if used)
- Project README
- Vehicle analysis data (`vehicle_analysis_data.csv`, if generated)
- Regression metrics (`regression_metrics.csv`, if generated)
- Model summary (`model_summary.txt`, if generated)
- Data visualizations
- Analysis and conclusions

## Key Statistical Findings

The experiment examines the relationship between vehicle characteristics and fuel economy using descriptive statistics, correlation analysis, visualizations, and multiple linear regression.

The scatter plot and fitted trend lines are used to examine how vehicle weight relates to fuel economy across transmission groups. Boxplots compare fuel economy by transmission type and cylinder count.

The multiple linear regression model estimates fuel economy using weight, horsepower, displacement, and cylinder count. RMSE, MAE, and R-squared are used to summarize the model's fit to the observed data.

The final interpretation should be based on the actual correlation values, regression coefficients, statistical significance results, and calculated evaluation metrics produced by the notebook.
