# 🎬 Netflix Content Analysis — Power BI Dashboard


An end-to-end exploratory data analysis and interactive dashboard project built in **Microsoft Power BI**, analyzing Netflix's global content library across genres, countries, ratings, and release trends.

---

## 📁 Project Structure

```
netflix-powerbi-analysis/
│
├── Netflix_Analysis.pbix        # Main Power BI file
├── netflix_titles.csv           # Source dataset
├── README.md                    # Project documentation

```

---

## 🗂️ Dataset

**Source:** [Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)

| Property | Details |
|---|---|
| File | `netflix_titles.csv` |
| Rows | 8,809 titles |
| Columns | 12 |

### Column Descriptions

| Column | Description |
|---|---|
| `show_id` | Unique ID for each title |
| `type` | Movie or TV Show |
| `title` | Name of the content |
| `director` | Director(s) |
| `cast` | Cast members |
| `country` | Country of production |
| `date_added` | Date added on Netflix |
| `release_year` | Year of release |
| `rating` | Content rating (TV-MA, PG-13, etc.) |
| `duration` | Duration in minutes or seasons |
| `listed_in` | Genre(s) |
| `description` | Short description |

---

## 🔧 Data Preparation (Power Query)

Performed in **Power Query Editor** inside Power BI:

- Promoted headers and set correct column data types
- Handled **31% missing values** in the `cast` column
- Handled missing values in `director` and `country` columns
- Extracted `year` from `date_added` for time-series analysis
- Split multi-value `listed_in` and `country` columns for granular analysis
- Removed duplicates and standardized text casing

> ⚠️ A separate **Query Errors** step was tracked in Power Query to monitor transformation issues.

---

## 📈 Key Insights

| Insight | Finding |
|---|---|
| 📌 Total Titles | **8,809** titles on Netflix |
| 🎬 Content Split | **69.62% Movies**, 30.38% TV Shows |
| 📅 Peak Year | Most content added around **2019–2020** |
| 🌍 Top Country | **United States** leads by a huge margin |
| 🇮🇳 India | **2nd largest** content contributor |
| 🎭 Top Genre | **Dramas, International Movies** (362 titles) |
| ⭐ Top Rating | **TV-MA** is the most common rating (36.41%) |
| 📉 Older Content | Very little content pre-2010 |

---

## 🖥️ Dashboard Pages

### Page 1 — Netflix Content Overview

| Visual | Description |
|---|---|
| KPI Card | Total Netflix titles |
| Line Chart | Content added per year (2008–2021) |
| Pie Chart | Movies vs TV Shows split |
| Map Visual | Global content distribution by country |

### Page 2 — Netflix Advanced Analysis

| Visual | Description |
|---|---|
| Horizontal Bar Chart | Top genres by number of titles |
| Stacked Bar Chart | Movie vs TV Show added by release year |
| Donut Chart | Content rating distribution |
| Horizontal Bar Chart | Top 10 countries with most content |

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/netflix-powerbi-analysis.git
   cd netflix-powerbi-analysis
   ```

2. **Open in Power BI Desktop**
   - Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
   - Open `Netflix_Analysis.pbix`

3. **Refresh Data (if needed)**
   - Go to `Home > Transform Data`
   - Update the file path in the Source step to point to your local `netflix_titles.csv`
   - Click `Close & Apply`

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Microsoft Power BI Desktop | Dashboard creation & data modeling |
| Power Query (M Language) | Data cleaning & transformation |
| DAX | Calculated measures & KPIs |
| Bing Maps Visual | Geographic distribution |
| Excel / CSV | Source data |

---

## 📌 Features

- ✅ Interactive slicers and cross-filtering across visuals
- ✅ Drill-through enabled between pages
- ✅ Dynamic KPI cards
- ✅ Time-series trend analysis
- ✅ Geographic map visualization
- ✅ Content rating breakdown
- ✅ Genre analysis with horizontal bar charts

---



> ⭐ If you found this project helpful, please give it a star!

