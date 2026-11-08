# Feature Encoding

Turning categorical columns into numbers, with three encoders and when to use each.

## `feature-encoding.ipynb`

| Encoding | Methods | Applied to | Use when |
|---|---|---|---|
| One-hot | `pd.get_dummies`, `OneHotEncoder` (with `drop='first'`) | Tips (`sex`, `smoker`, `day`, `time`) and T-shirts (`Brand`, `Color`, `Design`, `Delivery status`) | Categories have no order and there are few of them |
| Binary | `category_encoders.BinaryEncoder` | Gapminder (`country`, `continent`, `iso_alpha`) | A column has many categories: 19 columns here, instead of 288 with one-hot |
| Ordinal | a `dict` with `.map()`, `OrdinalEncoder` | T-shirts `Size` (XS < S < M < L < XL < XXL) | Categories have a natural order |

Each encoder is shown in two ways where possible (plain `pandas` and `scikit-learn`), and the encoded columns are joined back to the original data.

## Datasets

- Tips and Gapminder come with Plotly (`px.data`)
- `dataset/t-shirts.csv`: 500 T-shirt orders

## How to run

```bash
pip install -r requirements.txt
jupyter notebook feature-encoding.ipynb
```

**Tools:** Python · Jupyter Notebook · pandas · NumPy · scikit-learn · category_encoders · Plotly
