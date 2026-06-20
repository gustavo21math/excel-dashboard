# Global Music Streaming Analytics Dashboard

## 📊 Project Overview

This project is an interactive Excel dashboard built on Kaggle data about global music streaming trends and listener behavior. It lets you explore genre preferences, geographic distribution, platform usage, and listening habits across **50,000 listener and session records** — all without writing code. The goal is a reproducible, portfolio-ready analytics deliverable that demonstrates end-to-end Excel data skills.

## 🎯 Skills Demonstrated

- **Power Query** — import, type casting, cleaning, and loading data from CSV
- **Pivot Tables** — aggregations that feed charts and KPIs
- **Slicers** — interactive filters for country and platform
- **KPI Cards** — summary metrics displayed as dashboard tiles
- **Charts** — bar charts for genre and platform rankings
- **Map Visualization** — geospatial view of listener distribution by country
- **Excel Formulas** — `AVERAGE`, `COUNTIF`, and related logic for custom metrics
- **Git + GitHub** — version control and project publication

## 🔧 How It Works

The dashboard uses slicers to filter the underlying dataset by **country** and **platform**. When you change a filter, KPI cards and charts update dynamically across the full 50,000-record dataset.

Supporting workbook sheets handle the data model:

- `calculator` — KPI calculations
- `platform` — platform-level aggregations
- `country` / `country_dashboard` — country metrics and map view
- `avg minutes` — listening time metrics

The GIF below shows real-time interaction: applying filters by country, platform, and genre, and watching the KPIs respond.

![Dashboard demo](docs/screenshots/dashboard.gif)

## 📈 Data & Methodology

| Item | Details |
|------|---------|
| **Source** | [Global Music Streaming Trends & Listener Insights](https://www.kaggle.com/datasets/atharvasoundankar/global-music-streaming-trends-and-listener-insights) (Kaggle) |
| **Author** | Atharva Soundankar |
| **Records** | 50,000 listener/session rows |
| **Raw CSV** | Not versioned in this repo — download from Kaggle |

**Power Query workflow:**

1. Import the CSV from Kaggle
2. Set column data types (text, numeric, date)
3. Standardize categories (e.g. platform and genre names)
4. Handle nulls and inconsistent values
5. Load the clean model to the data sheet

For a detailed build walkthrough (in Spanish), see [`docs/process.md`](docs/process.md).

## 📸 Dashboard Features

### KPI Cards

| KPI | Description |
|-----|-------------|
| **Avg Listening Time** | Average hours spent listening per session |
| **Premium Users** | Share of listeners on a premium subscription |
| **Repeat Song Rate** | How often users replay the same track |

### Visualizations

| Chart | Description |
|-------|-------------|
| **Top Genre** | Bar chart ranking the most-listened music genres |
| **Country Map** | Geospatial distribution of listeners by country |
| **Streaming Platform** | Bar chart comparing usage across platforms (Spotify, Apple Music, etc.) |

## 🚀 How to Use

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/atharvasoundankar/global-music-streaming-trends-and-listener-insights).
2. Open `dashboard/global-music-streaming-dashboard.xlsx`.
3. If needed, reconnect the data source via **Data > Get Data > From Text/CSV**.
4. Refresh all queries with **Refresh All**.
5. Use the slicers and verify that pivot tables, charts, and KPI cards update on the dashboard sheet.

## 📁 Files & Structure

```
excel/
├── README.md
├── dashboard/
│   └── global-music-streaming-dashboard.xlsx
├── docs/
│   ├── process.md              # Build process (Spanish)
│   └── screenshots/
│       └── dashboard.gif       # Interactive demo
└── .gitignore
```

### Workbook Sheets

| Sheet | Purpose |
|-------|---------|
| `Global_Music_Streaming_Listener` | Raw imported data from Kaggle |
| `calculator` | KPI calculations |
| `platform` | Platform aggregations |
| `country` | Country aggregations |
| `country_dashboard` | Map and country-level metrics |
| `avg minutes` | Listening time metrics |

## 💡 Key Findings

> *Key insights from the analysis will be added here. (Placeholder — specific findings to be provided.)*
