# QuickCart Market Basket Analysis

## Project overview
This unsupervised machine-learning project discovers products that are purchased together using **Apriori** and **FP-Growth**. It converts order line items into a basket matrix, mines frequent itemsets, generates association rules, validates six expected associations, and translates the results into business recommendations.

## Dataset
- `data/quickcart_basket_transactions.csv` — transaction line items
- `data/dim_skus.csv` — 60-item product catalog
- `data/frequent_itemsets.csv` — supplied reference itemsets
- `data/association_rules_full.csv` — supplied reference rules
- `QuickCart_MarketBasket_Project_Spec.pdf` — original project brief

## Main notebook
Open `QuickCart_Market_Basket_Analysis.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab. Run cells from top to bottom. The notebook installs required libraries if missing.

## Technologies
- Python
- Pandas and NumPy
- mlxtend (TransactionEncoder, Apriori, FP-Growth, association_rules)
- Matplotlib
- Jupyter Notebook

## Key concepts
- **Support:** fraction of baskets containing an itemset or rule.
- **Confidence:** probability of the consequent given the antecedent.
- **Lift:** how much more often the consequent occurs with the antecedent than expected by chance.
- **Apriori:** mines frequent itemsets by generating candidate itemsets.
- **FP-Growth:** mines frequent itemsets using a frequent-pattern tree.

## Run locally
```bash
python -m pip install -r requirements.txt
jupyter notebook
```
Open `QuickCart_Market_Basket_Analysis.ipynb` and run all cells.

## Outputs
When the notebook is run, it creates an `outputs/` directory containing:
- `frequent_itemsets_apriori.csv`
- `frequent_itemsets_fpgrowth.csv`
- `association_rules.csv`
- `actionable_rules.csv`
- `expected_pattern_validation.csv`
- `business_recommendations.csv`

## Important note
Association rules reveal co-purchase patterns; they do not prove causation. Very high lift with very low support should be interpreted cautiously.
