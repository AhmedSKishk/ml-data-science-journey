# Handling Outliers

Detecting and handling outliers in the Titanic `Fare` column.

## `handling-outliers.ipynb`

| Step | Method |
|---|---|
| Inspect the distribution | Plotly histogram of `Fare` |
| Detect outliers | `datasist.detect_outliers`, based on IQR rule (values beyond 1.5 × IQR from Q1/Q3) |
| Treatment 1 | Drop the rows that contain outliers |
| Treatment 2 | Replace the outlier values with the column median |
| Custom detector | `custom_outliers()`: flags values outside chosen percentiles (default 10th and 90th) |

The custom function takes the bounds as parameters, so the number of flagged rows changes with the range:

| Percentile range | Rows flagged |
|---|---|
| 0.10 – 0.90 | 175 |
| 0.10 – 0.99 | 97 |

## Dataset

`datasets/Titanic.csv`

**Tools:** Python · Jupyter Notebook · pandas · NumPy · Plotly · datasist