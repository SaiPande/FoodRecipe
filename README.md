Preprocess & EDA

Files created:
- `preprocess_and_eda.py` – main script that: loads CSV, parses ingredient lists, drops columns with >70% missing, imputes missing values, flags outliers, creates features, generates EDA plots, and writes:
  - `cleaned_recipes.csv`
  - `recipes_for_rag.jsonl`
  - `eda/` (plots)
  - `selected_features.csv`

Dependencies:
- See `requirements.txt`. Install with:

```powershell
pip install -r archive\requirements.txt
```

Run:

```powershell
python archive\preprocess_and_eda.py
```

Notes & next steps:
- The script flags outliers (IQR). To apply winsorization, change `FLAG_OUTLIERS_ONLY = False` at top of the script.
- For Graph RAG: `recipes_for_rag.jsonl` is newline-delimited JSON objects with `id`, `text`, and `metadata`. This is ready for chunking and ingestion into a vector DB / retriever.
- If you want, I can run the script here (will attempt to `pip install` packages and execute). Confirm and I will proceed to run it and report results (or run only if you prefer).