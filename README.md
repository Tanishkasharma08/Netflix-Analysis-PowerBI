🎬 Netflix Content Analysis — Power BI Dashboard

An end-to-end exploratory data analysis and interactive dashboard project built in Microsoft Power BI, analyzing Netflix's global content library across genres, countries, ratings, and release trends.

📊 Dashboard Preview
Page 1 — Content Overview
<img width="1158" height="647" alt="{610DBBEF-0E36-43D7-A6BB-118CE86CB411}" src="https://github.com/user-attachments/assets/5a5d9e42-afb1-4cf9-9c12-2b071896b442" />


Total Netflix Titles: 8,809
Content added over time (2008–2021)
Movies vs TV Shows distribution
Global content distribution map

Page 2 — Advanced Analysis
<img width="1154" height="667" alt="{C6F97A36-4502-4380-BB12-6DF26C798506}" src="https://github.com/user-attachments/assets/57e101e6-456e-4441-ac68-f7e8a1e6fc4f" />


Top genres on Netflix
Movie vs TV Show added by year
Content rating distribution
Top 10 countries with most Netflix content


📁 Project Structure
netflix-powerbi-analysis/
│
├── Netflix_Analysis.pbix        # Main Power BI file
├── netflix_titles.csv           # Source dataset
├── README.md                    # Project documentation
└── screenshots/
    ├── overview.png
    └── advanced.png

🗂️ Dataset

Source: Netflix Movies and TV Shows — Kaggle
File: netflix_titles.csv
Rows: 8,809 titles
Columns: 12

ColumnDescriptionshow_idUnique ID for each titletypeMovie or TV ShowtitleName of the contentdirectorDirector(s)castCast memberscountryCountry of productiondate_addedDate added on Netflixrelease_yearYear of releaseratingContent rating (TV-MA, PG-13, etc.)durationDuration in minutes or seasonslisted_inGenre(s)descriptionShort description

🔧 Data Preparation (Power Query)
Performed in Power Query Editor inside Power BI:

Promoted headers and set correct column data types
Handled 31% missing values in the cast column
Handled missing values in director and country columns
Extracted year from date_added for time-series analysis
Split multi-value listed_in and country columns for granular analysis
Removed duplicates and standardized text casing


⚠️ A separate Query Errors step was tracked in Power Query to monitor transformation issues.


📈 Key Insights
InsightFinding📌 Total Titles8,809 titles on Netflix🎬 Content Split69.62% Movies, 30.38% TV Shows📅 Peak YearMost content added around 2019–2020🌍 Top CountryUnited States leads by a huge margin🇮🇳 India2nd largest content contributor🎭 Top GenreDramas, International Movies (362 titles)⭐ Top RatingTV-MA is the most common rating (36.41%)📉 Older ContentVery little content pre-2010

🖥️ Dashboard Pages
Page 1: Netflix Content Overview
VisualDescriptionKPI CardTotal Netflix titlesLine ChartContent added per year (2008–2021)Pie ChartMovies vs TV Shows splitMap VisualGlobal content distribution by country
Page 2: Netflix Advanced Analysis
VisualDescriptionHorizontal Bar ChartTop genres by number of titlesStacked Bar ChartMovie vs TV Show added by release yearDonut ChartContent rating distributionHorizontal Bar ChartTop 10 countries with most content

🚀 How to Run

Clone the repository

bash   git clone https://github.com/your-username/netflix-powerbi-analysis.git
   cd netflix-powerbi-analysis

Open in Power BI Desktop

Download and install Power BI Desktop (free)
Open Netflix_Analysis.pbix


Refresh Data (if needed)

Go to Home > Transform Data
Update the file path in the Source step to point to your local netflix_titles.csv
Click Close & Apply




🛠️ Tools & Technologies
ToolPurposeMicrosoft Power BI DesktopDashboard creation & data modelingPower Query (M Language)Data cleaning & transformationDAXCalculated measures & KPIsBing Maps VisualGeographic distributionExcel / CSVSource data

📌 Features

✅ Interactive slicers and cross-filtering across visuals
✅ Drill-through enabled between pages
✅ Dynamic KPI cards
✅ Time-series trend analysis
✅ Geographic map visualization
✅ Content rating breakdown
✅ Genre analysis with horizontal bar charts
