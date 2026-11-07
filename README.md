# DoE_Rxn_analysis
A notebook for reaction optimisation that generates Box–Behnken DoE designs to inform experimental work, fits a quadratic response surface, and plots the results for ease of interpretation.
## Requirements

- Python 3
- pandas
- NumPy
- pyDOE3
- statsmodels
- matplotlib

## Usage

1. **Enter the settings** in the first cell:

```python
centre_points = 3          # 3 default

response_var = "yield_pct"  # some response

factors = {
    "temp":    {"low": 20,  "medium": 50,  "high": 75, "units": "C"},
    "cat_mol": {"low": 0.1, "medium": 0.5, "high": 1,  "units": "mol %"},
    "A_equiv": {"low": 1,   "medium": 5,   "high": 10, "units": "equiv"},
}

results = []               # leave empty until the experiments are done
```

   At least three factors are needed, each with `low < medium < high`. Names exlcuded include anything with % signs and only `yield`).
