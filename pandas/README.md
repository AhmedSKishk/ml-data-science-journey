# Pandas

Pandas exercises covering DataFrame creation, data selection, filtering, and manipulation.

## `pandas-1.ipynb`

| Task | Method Used |
| Build a DataFrame from dict + custom index | `pd.DataFrame()`, `pd.Index()` |
| Select specific columns | `.loc[]`, column indexing |
| Add a new calculated column | Vectorized column arithmetic |
| Filter rows by condition | Boolean indexing |
| Drop rows and columns | `.drop()` |
| Find min, max, and range | `.min()`, `.max()` |
| Export to CSV | `.to_csv()` |

**Tools:** Python · Jupyter Notebook · pandas · NumPy

---

## `pandas-2.ipynb`

| Task | Method Used |

| Group and aggregate (sum, mean, count) | `.groupby()`, `.sum()`, `.mean()`, `.count()` |
| Count unique values per category | `.value_counts()`, `.nunique()` |
| Handle missing values in grouped data | `NaN` handling with `.count()` vs `.size()` |
| Multi-level grouping (by 2+ columns) | `.groupby([...])` |
| Reshape data between long and wide formats | `.unstack()`, `pd.pivot_table()` |
| Weighted average calculation | Custom aggregation with `.sum()` |
| Load real-world dataset from CSV | `pd.read_csv()` |

**Tools:** Python · Jupyter Notebook · pandas · NumPy