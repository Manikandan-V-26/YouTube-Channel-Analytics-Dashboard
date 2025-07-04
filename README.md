# 📺 YouTube Channel Analytics Dashboard

This project is a *real-world end-to-end data analytics solution* built using *Python* for data scraping and initial cleaning, and *Power BI* for advanced cleaning, DAX modeling, and dashboarding. It provides insights into the *Top 100 Global YouTube Channels*, analyzing metrics like total subscribers, total views, and category-wise performance.

---

## 📌 Project Overview

- *Objective*: To analyze the top 100 YouTube channels globally using publicly available data and extract business intelligence insights.
- *Tools Used*:
  - 🐍 Python (Selenium, Pandas, NumPy)
  - 📊 Power BI (M Query, DAX, Visualizations)
  - 📂 CSV for data transfer

---

## 🛠 Tools & Technologies

| Purpose               | Tool / Library            |
|------------------------|---------------------------|
| Data Collection        | Selenium (Python)         |
| Data Cleaning          | Pandas, NumPy (Python) + M Query (Power BI) |
| Data Modeling          | DAX (Power BI)            |
| Data Visualization     | Power BI (Desktop)        |
| Language               | Python 3.x                |
| Output Format          | .pbix, .csv, .ipynb |

---

## 🔍 Python Workflow (Data Cleaning.ipynb)

1. *Web Scraping*:
   - Scraped data from [Noxinfluencer Top 100](https://www.noxinfluencer.com/youtube-channel-rank/top-100-global) using Selenium.
   - Saved as raw .csv file.

2. *Initial Data Cleaning*:
   - Removed nulls, duplicates, and outliers.
   - Converted subscriber/view counts to numeric format.
   - Standardized column data types using .astype().
   - Exported cleaned file: Cleaned_Dataset.csv

---

## 🧼 Power BI Cleaning (M Query)

- Trimmed whitespace in Channel Name using Text.Trim
- Removed unwanted symbols from text columns using Text.Replace
- Renamed columns for consistency
- Handled empty rows using *Fill Down* and *Replace Values*
- Ensured proper data types for all columns

---

## 📐 Data Modeling with DAX

Created custom KPIs and summary measures:
dax
Total Subscribers = SUM('Cleaned_Dataset'[Subscribers])
Average Views = AVERAGE('Cleaned_Dataset'[Views])
Channel Count = COUNTROWS('Cleaned_Dataset')
Total Views = SUM('Cleaned_Dataset'[Views])

## 📊 Power BI Dashboard Features

- 💡 *KPI Cards*:
  - Total Subscribers
  - Total Views
  - Average Views per Channel
  - Total Channels Analyzed

- 📈 *Visualizations*:
  - Top 10 Channels by Subscribers
  - Average Views by Channel Category
  - Donut Chart: Subscriber Share by Category
  - Line + Column Chart: Impact of Categories on Views/Subs
  - Slicer to filter by Channel Category

- 🎨 *Design*:
  - YouTube-themed color palette
  - Custom background
  - Font & spacing optimized for clarity

---

## 📷 Dashboard Preview

![Dashboard Screenshot](https://github.com/Manikandan-V-26/YouTube-Channel-Analytics-Dashboard/blob/main/Dashboard.png) 

---

### 📁 Project Structure

| File / Folder                          | Description                               |
|----------------------------------------|-------------------------------------------|
| Cleaned_Dataset_scraper.py          | Python script to scrape and clean data    |
| Cleaned_Dataset.csv                 | Final cleaned dataset                     |
| YouTube_Analytics_Dashboard.pbix    | Final Power BI dashboard                  |
| README.md                            | This documentation file                   |
| images/                              | Folder containing dashboard images        |
| images/dashboard_screenshot.png     | Dashboard image preview                   |

