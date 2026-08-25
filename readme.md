# Freight Rate Prediction

Solution for the freight rate take-home. The model lives in one notebook.

## Files to submit

| File | What it is |
| --- | --- |
| `freight_rate.ipynb` | Solution code (explore, clean, split, train, predict) |
| `requirements.txt` | Python dependencies |
| `validation_predictions.csv` | 12,000 rows: `load_id,predicted_rate` |
| `Freight_Rate_Report.docx` | Split/validation write-up plus the December chart |

`score.py` is the provided scorer. It checks the prediction files and writes `scorer_results/candidate_december.png`.

## How to run

From this folder:

```bash
python -m pip install -r requirements.txt
jupyter notebook freight_rate.ipynb
```

Run all cells from top to bottom. The notebook writes `validation_predictions.csv` and fills `data/december_chart_inputs.csv`, then runs:

```bash
python score.py --predictions validation_predictions.csv --december-predictions data/december_chart_inputs.csv
```


