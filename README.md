# TP2 - Open Science: Biology Data Analysis

## Objective
This project demonstrates a complete workflow for analyzing biological data using Python, Pandas, NumPy, and Matplotlib. The goals are:

- Load and inspect biological data from a CSV file.
- Perform statistical analysis (mean, standard deviation, group comparison).
- Normalize and categorize data.
- Visualize the data using bar charts, boxplots, and scatter plots.
- Save the processed results for further analysis.

## Project Files
- `data_biology.csv` : Raw dataset with samples, cell counts, protein levels, growth rates, temperature, and groups.  
- `analysis.ipynb` : Jupyter Notebook containing the full analysis and plots.  
- `results_biology.csv` : Output CSV file after processing and adding new columns.  
- `README.md` : This file explaining the project.

## Steps Performed in the Notebook
1. Load the data with Pandas.  
2. Inspect the dataset using `info()`, `describe()`, and column selection.  
3. Filter data by group (e.g., "Treated").  
4. Compute basic statistics with NumPy (`mean`, `std`).  
5. Group data by `group` and compute the mean of `cell_count`.  
6. Normalize the `growth_rate` column.  
7. Categorize protein levels as "High" or "Normal" based on threshold.  
8. Visualize data:
   - Bar chart: cell count per sample  
   - Boxplot: cell count by group  
   - Scatter plot: growth rate vs temperature  
9. Convert selected columns to a NumPy array.  
10. Compute correlation between numeric columns.  
11. Save the processed DataFrame to `results_biology.csv`.

## Notes
- Make sure `data_biology.csv` is in the same folder as the notebook.  
- If encoding issues occur on Windows, use:
```python
df = pd.read_csv("data_biology.csv", encoding="latin1")
