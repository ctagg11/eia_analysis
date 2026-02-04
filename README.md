#  EIA Hourly Load Analysis (PJM Region)

This project pulls, cleans, and visualizes historical hourly electricity load data from the U.S. Energy Information Administration (EIA). It specifically focuses on the **PJM Interconnection (PJM)** region, which manages the high-voltage electric grid for all or parts of 13 Mid-Atlantic and Midwestern states.

## Features
- **Automated Data Retrieval:** Fetches hourly load data via the EIA v2 API.
- **Efficient Caching:** Saves downloaded data to a local CSV to prevent redundant API calls.
- **Data Cleaning:** Filters out anomalies and outliers (e.g., values outside the 65,000–170,000 MW range) and handles missing values.
- **Visualization:** (In Progress) Includes imports for time-series plotting and animations using Matplotlib.

## Prerequisites & Setup

### 1. EIA API Key
To run this notebook, you need a free API key from the EIA.
- Register here: [https://www.eia.gov/opendata/register.php](https://www.eia.gov/opendata/register.php)

### 2. Google Colab Secrets (Recommended)
This notebook is designed to keep your API key secure. 
1. Open the notebook in **Google Colab**.
2. Click the **Key icon (Secrets)** in the left sidebar.
3. Add a new secret:
   - **Name:** `EIA_API_KEY`
   - **Value:** *Paste your API key here*
4. Toggle **Notebook Access** to "On".

## Usage
The main configuration is located at the top of the notebook:
```python
REGION = "PJM"
START_DATE = "2023-01-01T00"
END_DATE   = "2025-12-31T23"
