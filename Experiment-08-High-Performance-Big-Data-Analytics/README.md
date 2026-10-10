# Experiment 08 — High-Performance Big Data Analytics Using R

## Domain

Transportation Analytics

## Objective

The objective of this experiment is to analyze large-scale NYC Yellow Taxi Trip data using efficient R programming techniques. The experiment compares data manipulation, functional programming, vectorized operations, sequential processing and parallel computing.

## Dataset

**NYC Taxi & Limousine Commission (TLC) — Yellow Taxi Trip Records**

Official source: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

## Tasks Performed

### Task 1 — Data Acquisition and Preparation
- Imported NYC Yellow Taxi Trip data.
- Inspected and cleaned the dataset.
- Extracted temporal features.
- Joined trip records with the Taxi Zone Lookup Table.

### Task 2 — Transportation Data Analytics
- Analysed trips by hour and weekday.
- Calculated fare and revenue summaries.
- Identified frequent and high-revenue routes.
- Examined payment preferences and trip distances.

### Task 3 — Efficient R Programming
- Implemented functional programming using `lapply()` and `purrr::map()`.
- Compared base R, vectorized operations and `data.table`.
- Benchmarked execution times.

### Task 4 — Parallel Computing
- Compared sequential and parallel processing.
- Used `foreach` and `doParallel`.
- Calculated execution speedup.

### Task 5 — Visualization and Performance Analysis
- Created visualizations using `ggplot2`.
- Compared execution time and approximate memory usage.
- Discussed scalability and performance trade-offs.

## Technologies

- R
- data.table
- ggplot2
- foreach
- doParallel
- microbenchmark
- purrr
- lubridate

## Deliverables

- R notebook
- PDF report
- Benchmark results
- Data visualizations
- Performance analysis and conclusion
