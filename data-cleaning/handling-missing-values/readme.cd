# Handling Missing Values

Finding and handling missing values on three datasets: Titanic, Sendy logistics, and UFO sightings.

## `handling-missing-values.ipynb`

For each dataset, the missing values are counted (count and percentage per column), 
    then each column gets a treatment based on how much is missing.

| Dataset | Column | Missing | Treatment | Why |
|---|---|---|---|---|
| Titanic | `Cabin` | 687 (77.10%) | Drop the column | Too much is missing to fill reliably |
| Titanic | `Embarked` | 2 (0.22%) | Drop the rows | Only two rows are affected |
| Titanic | `Age` | 177 (19.87%) | Fill with the median per `Sex` and `Pclass` | The median is robust to skew, 
    and grouping keeps the differences between passenger groups |
| Sendy logistics | `Precipitation in millimeters` | 20,649 (97.40%) | Drop the column | Almost empty |
| Sendy logistics | `Temperature` | 4,366 (20.59%) | `KNNImputer` (k = 5) | Estimates the value from similar rows |
| UFO | `Colors Reported` | 15,359 (84.20%) | Drop the column | Mostly empty |
| UFO | `Shape Reported` | 2,644 (14.49%) | Fill with `'OTHER'` | Reuses the dataset's own "unknown" category |
| UFO | `City` | 26 (0.14%) | Fill with the mode | Tiny share of rows |

Histograms of `Age` and `Temperature` are plotted before and after filling to check that the distribution is preserved.

## Datasets

`datasets/Titanic.csv` · `datasets/sendy_logistics.csv` · `datasets/ufo.csv`

**Tools:** Python · Jupyter Notebook · pandas · NumPy · Plotly · scikit-learn