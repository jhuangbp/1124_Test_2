<h1 align="center">
  <br>
  Army Recreation Machine Program (ARMP) - Exploratory Data Analysis
  <br>
</h1>

<h4 align="center">Comprehensive exploratory data analysis of military slot machine revenue, assets, and financial statements across U.S. military bases worldwide (FY2016–FY2024).</h4>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#project-description">Project Description</a> •
  <a href="#data-locations">Data Locations</a>
</p>

## Key Features

This directory contains eight comprehensive Jupyter notebooks analyzing slot machine operations across U.S. military installations:

* **District_Revenue_EDA.ipynb** - Base Revenue Ranking & Trends (FY2020–FY2024)
  - Analyzes which military bases generate the highest total revenue
  - Examines revenue ranking evolution by year and service branch (Army, Navy, Marine Corps)
  - Identifies geographic concentration of revenue (Korea and Japan dominate with >70% of total)

* **EGM_Distribution_EDA.ipynb** - FY2024 Asset Distribution Analysis
  - Visualizes EGM (Electronic Gaming Machine) distribution by region and service
  - Europe holds 39.4% of EGMs, Japan 37.8%, Korea 22.8%
  - Army operates 55.7% of all EGMs globally

* **EGM_Analysis_by_Region_Manufacturer_EDA.ipynb** - FY2021 Asset Report Analysis
  - Explores slot machine inventory by manufacturer (NOV, BAL, IGT, AIN, ITC)
  - Analyzes installation year trends and machine age distribution
  - Estimates revenue by base using machine counts and regional revenue data

* **Financial_Statements_EDA.ipynb** - ARMP Financial Analysis
  - Tracks operational cash vs total equity trends (2020–2024)
  - Analyzes asset depreciation and total asset value changes
  - Identifies unusual patterns (e.g., frozen equity values since 10/31/2021)

* **Marine_Revenue_EDA.ipynb** - Marine Corps Revenue Analysis
  - Examines revenue distribution and trends across Marine installations
  - Identifies seasonal patterns (higher gambling in March and May)
  - Shows COVID-19 impact (sharp revenue drop in 2020)

* **Navy_Slot_NAFI_Revenue_Comparison_EDA.ipynb** - Navy Revenue Comparison (FY2016–FY2022)
  - Compares Slot Revenue vs NAFI Reimbursements across countries
  - Japan dominates Navy revenues, far surpassing all other countries
  - Demonstrates consistent growth trend through FY2022

* **Navy_Slot_Revenue_by_Installation_EDA.ipynb** - Navy Installation-Level Analysis (FY2018–FY2024)
  - Identifies top-performing installations (Yokosuka and Sasebo in Japan)
  - Analyzes average slot revenue per installation by country
  - Japan shows highest average revenue per installation

* **Revenue_Comparison_EDA.ipynb** - Cross-Service Revenue Analysis
  - Consolidates slot machine revenue across Army, Navy, and Marine Corps
  - Europe generates largest total revenue (~$41M), followed by Far East (~$30M)
  - Estimates manufacturer revenue contribution using machine counts

## How To Use

To run these analyses, you'll need Python 3.x with the following libraries:

```bash
# Install required packages
pip install pandas numpy matplotlib seaborn jupyter

# Navigate to the eda directory
cd fa25-team-b/eda

# Launch Jupyter Notebook
jupyter notebook
```

Each notebook is self-contained and can be run independently. Data files should be placed in the appropriate locations as referenced in each notebook.

**Data Cleaning Notes:**
- Numeric fiscal values: Cleaned by removing `$`, commas, and special characters; parentheses converted to negative values
- Date columns: Normalized to `YYYY-MM` or `YYYY-MM-DD` format using pandas datetime parsing
- Missing values: Replaced with `0.0` for revenue columns or empty strings for text fields
- Outliers: Removed using IQR (Interquartile Range) method for visualization purposes

## Project Description

This exploratory data analysis examines the **Army Recreation Machine Program (ARMP)**, which operates slot machines at U.S. military installations across Europe, Japan, and Korea. The analysis covers:

* **Revenue Analysis**: Slot machine revenue trends from FY2016 to FY2024 across service branches and geographic regions
* **Asset Distribution**: Electronic Gaming Machine (EGM) inventory, manufacturer composition, and installation year patterns
* **Financial Health**: Operational cash flow, asset depreciation, and equity trends from consolidated financial statements
* **Geographic Insights**: Regional revenue concentration and base-level performance rankings
* **Temporal Trends**: Seasonal patterns, COVID-19 impacts, and year-over-year growth analysis

**Key Findings:**
- Far East bases (Korea + Japan) contribute over 70% of total ARMP slot machine revenue
- Army bases collectively generate nearly 60% of global revenue
- Europe holds the largest share of EGMs (39.4%) followed by Japan (37.8%)
- Japan's Navy installations (Yokosuka, Sasebo) are top revenue generators
- Operational cash declined sharply in 2023 due to depletion of restricted cash reserves
- Total equity has remained frozen at the exact same value since October 31, 2021

## Data Locations

All datasets are derived from ARMP official reports obtained through FOIA requests:

* **District Revenue Data (FY2020–FY2024)**: `District_Revenue_filtered_FY20-FY24_final.csv`
  - Monthly revenue by base, region, and service branch

* **Marine Revenue Data (FY2020–FY2024)**: `Marine_Revenue_FY20-FY24_detail.csv`
  - Detailed Marine Corps installation revenue with NAFI amounts

* **Navy Revenue Reports**:
  - `navy_slot_results.csv` - Slot revenue by country and installation (FY2016–FY2022)
  - `navy_nafi_reimbursements.csv` - NAFI reimbursement data (FY2016–FY2022)
  - `monthly_summary_final.csv` - Monthly revenue breakdown (FY2018–FY2024)

* **Asset Reports**:
  - `FY2021_Asset_Report.xlsx` - Complete asset inventory with manufacturer details
  - `egms_by_region_service_2024.csv` - FY2024 EGM distribution by region and service

* **Financial Statements**: `FinancialStatement.csv`
  - Monthly asset/liability balance, cash flow, and equity data

**Note**: Due to the sensitive nature of the data, actual file paths and storage locations may vary. Consult project documentation for specific data access instructions.

