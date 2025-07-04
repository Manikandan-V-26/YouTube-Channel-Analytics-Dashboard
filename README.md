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
   - Exported cleaned file: Top_100_youtube.csv

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
```dax
Total Subscribers = SUM('Top_100_youtube'[Subscribers])
Average Views = AVERAGE('Top_100_youtube'[Views])
Channel Count = COUNTROWS('Top_100_youtube')
Total Views = SUM('Top_100_youtube'[Views])

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

![Dashboard Screenshot](dashboard_screenshot.png) 

---

