# Meridian — Retail Intelligence & Sales Forecasting

**An interactive retail analytics and AI-powered sales forecasting project** built with Python, machine learning, and a lightweight web dashboard.

> **Live Demo:** Add your deployed website URL here  
> **Dataset:** Retail sales dataset containing approximately 73,000 records

## Overview

Meridian is a retail decision-support dashboard designed to explore sales performance, discover patterns, compare forecasting models, and segment stores. It combines a Python analytics pipeline with an interactive, browser-based dashboard.

## Features

- **Sales analytics:** Explore revenue and sales performance across stores, products, brands, and categories.
- **Trend analysis:** Review daily, monthly, and year-over-year sales patterns.
- **Forecasting:** Compare forecasting approaches using rolling-origin backtesting and view forecast intervals.
- **Store segmentation:** Use K-Means clustering to group stores by performance and behaviour.
- **Discount analysis:** Explore the relationship between discounts and sales volume.
- **Interactive dashboard:** Use filters, charts, a what-if simulator, and the “Ask Meridian” query box.
- **Data quality checks:** Generate a report of data integrity checks and potential issues.
- **Exported outputs:** Review forecast results, model comparisons, store segments, and the written report.

## Technology Stack

- Python
- pandas and NumPy
- SciPy
- scikit-learn
- HTML, CSS, and JavaScript
- SVG-based visualizations

## Project Structure

```text
meridian-retail-forecasting/
├── data/
│   └── Retail_Sales_Data_Unlox.csv
├── src/
│   ├── etl.py
│   ├── analytics.py
│   ├── forecasting.py
│   ├── segmentation.py
│   ├── insights.py
│   ├── report.py
│   ├── build.py
│   └── config.py
├── web/
│   ├── index.html
│   ├── style.css
│   ├── app.js
│   └── data.js
├── outputs/
│   ├── REPORT.md
│   ├── forecast_daily.csv
│   ├── model_leaderboard.csv
│   ├── store_segments.csv
│   └── data_quality_report.csv
├── requirements.txt
├── run.py
└── README.md
```

## Getting Started

### 1. Clone the repository

Replace `YOUR-USERNAME` with your GitHub username.

```bash
git clone https://github.com/YOUR-USERNAME/meridian-retail-forecasting.git
cd meridian-retail-forecasting
```

### 2. Create and activate a virtual environment (recommended)

**Windows PowerShell**
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, you can run the commands below using `python` without activating the environment, or use Command Prompt activation:

```bat
.venv\Scripts\activate.bat
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Run the project

```bash
python run.py
```

The script serves the dashboard locally and attempts to open it in your browser. The default local address is:

```text
http://127.0.0.1:8765/index.html
```

To rebuild the analytics and dashboard data from the dataset:

```bash
python run.py --rebuild
```

To use a different compatible CSV or Excel dataset:

```bash
python run.py --data path/to/your_dataset.csv
```

The replacement dataset must contain the columns expected by the project's ETL pipeline.

## Outputs

The project generates or includes files such as:

- `outputs/REPORT.md` — summary of findings and methodology
- `outputs/forecast_daily.csv` — daily forecast output
- `outputs/model_leaderboard.csv` — model comparison results
- `outputs/store_segments.csv` — store segmentation results
- `outputs/data_quality_report.csv` — data quality checks

## Deploying the Dashboard

The files in `web/` form the browser dashboard. For a **static website deployment**, publish the contents of the `web/` directory using a static hosting service such as Netlify or GitHub Pages. Confirm that `index.html`, `style.css`, `app.js`, and `data.js` are uploaded and that the dashboard loads correctly.

**Note:** Static hosting publishes the prebuilt dashboard only; it does not run the Python analytics pipeline. To regenerate forecasts or process new data online, deploy the Python application/pipeline separately on a suitable Python hosting service.

After deployment, replace the Live Demo placeholder at the top of this README with your public URL.

## Important Notes

- The dashboard can be opened locally from `web/index.html` if its generated data file is present.
- Running `python run.py --rebuild` requires the Python dependencies listed in `requirements.txt`.
- Do not commit API keys, passwords, private credentials, or sensitive data to GitHub.
- Check dataset licensing and permissions before publishing the dataset publicly.

## Learning Outcomes

This project provides practical experience with data cleaning, exploratory analysis, forecasting evaluation, clustering, interactive dashboard development, and communicating business insights from data.

## Author

**Your Name**  
GitHub: `https://github.com/YOUR-USERNAME`  
LinkedIn: Add your LinkedIn profile URL

## Tags

`Python` `MachineLearning` `RetailAnalytics` `SalesForecasting` `DataAnalytics` `KMeans` `Dashboard`
