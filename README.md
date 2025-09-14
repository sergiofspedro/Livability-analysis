# Porto Liveability Analysis

This repository contains a Jupyter Notebook (`PORTO_liveability_analysis.ipynb`) that calculates and visualizes a **Livability Index** for the city of Porto, Portugal. The analysis integrates multiple urban indicators (transport, culture, economy, inequality, pollution, housing, health, and environment) into a single standardized and weighted measure of city livability.

## 📑 Overview

The notebook performs the following steps:

1. **Data Import**
   - Loads CSV datasets from Google Drive containing urban indicators across multiple domains:
     - Transport & Communications
     - Culture & Leisure
     - Economic Vitality
     - Inequality & Commuting Time
     - Security & Pollution
     - Environment
     - Housing & Urban Regeneration
     - Health

2. **Preprocessing & Normalization**
   - Extracts relevant values from each dataset.
   - Standardizes each indicator using **Z-Score standardization**.
   - Applies domain-specific weights to each indicator.
   - Adjusts inequality and insecurity/pollution dimensions (negative contributors).

3. **Livability Index Calculation**
   - Computes a **weighted sum of Z-scores**.
   - Applies a **sigmoid transformation** to normalize results to a 0–1 scale.
   - Scales the final result to a **0–100 Livability Index**.

4. **Results & Export**
   - Creates a results table with all intermediate and final scores.
   - Exports results as a CSV file (`Porto_Global.csv`).

5. **Visualization**
   - Generates bar plots showing contributions of each dimension (positive in green, negative in red).
   - Saves plots as PNG images to Google Drive.
   - Computes correlation matrices between numerical indicators for further analysis.

## 📊 Outputs

- **CSV file**: `Porto_Global.csv` (contains weighted scores and the Livability Index).
- **Visualization**: `porto_livability_plot.png` (bar plot of overall and category scores).
- **Correlation matrix** (optional, depending on execution).

## ⚙️ Requirements

- Python 3.x
- Jupyter Notebook / Google Colab
- Packages:
  - `pandas`
  - `numpy`
  - `matplotlib`

## 🚀 How to Use

1. Upload the notebook to Google Colab.
2. Mount Google Drive to access the input CSV files.
3. Adjust file paths if needed.
4. Run all cells to compute and visualize the Porto Livability Index.

## 📌 Notes

- Input datasets must be available in the specified Google Drive folders.
- The weighting of factors is **custom-defined** (e.g., Environment: 20%, Health: 15%, Security/Pollution: 15%, etc.).
- The approach can be adapted to analyze other cities by replacing the datasets.
