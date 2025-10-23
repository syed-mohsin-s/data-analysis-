# Data Science Project – Fear & Greed Web3 Trader Analysis

This project analyzes historical trader data against the daily Fear & Greed Index to understand how market sentiment affects trader profitability, and activity.

The entire analysis is contained in the `notebook_1.ipynb` file, designed to be run in Google Colab.

## 🚀 How to Run This Project

1.  **Open in Google Colab**:
    * Click the link to open the notebook: https://colab.research.google.com/drive/1yvi8UQcQh059bNEPJfBkErwxTaaamAyV?usp=sharing
    * Save a copy in your own Drive.

2.  **Run the Notebook**:
    * Run the cells in order from top to bottom.
    * The notebook will automatically:
        1.  Create the `csv_files/` and `outputs/` directories.
        2.  Install all required Python libraries.
        3.  Download the two source datasets from Google Drive into `csv_files/`.
        4.  Clean, merge, and analyze the data.
        5.  Save all generated plots to the `outputs/` folder.
        6.  Save the final cleaned/merged dataset to `csv_files/`.

## 📁 Project Structure

This repository follows the required submission format:

```
ds_Syed mohsin/
├── notebook_1.ipynb          # The main (and only) analysis notebook.
├── csv_files/
│   ├── historical_data.csv       # Raw data (downloaded by notebook).
│   ├── fear_greed_index.csv    # Raw data (downloaded by notebook).
│   └── merged_trade_data.csv   # Cleaned, merged data (created by notebook).
├── outputs/
│   ├── pnl_distribution_plot.png
│   ├── profitability_vs_sentiment_barchart.png
│   ├── daily_cumulative_pnl_trend.png
│   ├── coin_sentiment_pnl_heatmap.png
│   ├── rolling_pnl_vs_sentiment.png
│   ├── rolling_trades_vs_sentiment.png
│   └── model_confusion_matrix.png
├── ds_report.pdf               # A PDF summary of the project insights (see below).
└── README.md                   # This file.
```

## 📊 Key Insights

The analysis concluded that trader profitability is significantly linked to market sentiment.

1.  **'Fear' is More Profitable**: Traders had a higher profitability rate (52.8% vs. 50.9%) and a higher median PnL ($\$0.16$ vs. $\$-0.27$) during 'Fear' days compared to 'Greed' days.
2.  **'Greed' Drives Volume**: 'Greed' periods saw a significant *increase in trade count* (activity), but this did not translate into better performance, suggesting FOMO-driven, less-profitable trading.
3.  **Statistical Significance**: Both a Mann-Whitney U test (for PnL magnitude) and a Chi-Square test (for profitability rate) confirmed these differences were statistically significant (p-value < 0.0001).

For a full summary, please see `ds_report.pdf`.

## ⚠️ Note on Missing Data

The project instructions mentioned analyzing `leverage` and `leverage_bins`. This feature was **not present** in the provided `historical_data.csv` file. Therefore, all analysis related to leverage was omitted.