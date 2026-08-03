# 🏏 IPL Analysis Dashboard (2008–2025)

An interactive **Power BI** dashboard that brings 18 seasons of the Indian Premier League to life — season winners, points tables, Orange & Purple Cap holders, six/four hitters, and overall tournament stats — all on a single, richly-designed page.

---

## 📌 Overview

This repository contains a single `.pbix` file — **`IPL_Dashboard.pbix`** — a self-contained Power BI report that visualizes historical IPL (Indian Premier League) match data from **2008 to 2025**. The dashboard is built for quick, at-a-glance storytelling: pick a season from the slicer and every card, image, and table on the page updates instantly.

> 📁 **File:** `IPL_Dashboard.pbix`
> 📊 **Type:** Single-page Power BI report (interactive `.pbix`)
> 🗓️ **Data Range:** 2008 – 2025 (all IPL seasons)

---

## 🖼️ Dashboard Preview

* [Link-to-my-image-here]((https://github.com/SugamSagar-DS458/IPL-Analysis-PowerBI_Dashboard/blob/main/IPL%20Dashboard.png))


## ✨ Features

The report is a single page (**"Page 1"**) composed of ~40 visuals, organized into the following sections:

| Section | Description |
|---|---|
| 🏷️ **Header / Branding** | Tata IPL logo, page title banner (*"IPL Analysis (2008–2025)"*), and background imagery |
| 🎚️ **Season Slicer** | Filter the entire report by a specific IPL season |
| 🏆 **Season Winner & Runner-Up** | Cards displaying the champion and runner-up team names with team logos, dynamically updating per selected season |
| 📊 **Tournament Summary Cards** | KPI cards for Total Matches, Total Teams, Total Venues, Total 4's, Total 6's, Centuries, and Half-Centuries |
| 🟠 **Orange Cap Stats** | Top run-scorer of the season — player name, team, runs, and photo |
| 🟣 **Purple Cap Stats** | Top wicket-taker of the season — player name, team, wickets, and photo |
| 🎯 **Total Fours** | Player with most fours in the season — name, team, count, and photo |
| 💥 **Total Sixes** | Player with most sixes in the season — name, team, count, and photo |
| 📋 **Points Table** | Full team-by-team standings: matches played, won, lost, tied, no-result, and total points, with team logos |
| 🔗 **Quick Links** | Clickable buttons linking to official IPL resources — [iplt20.com](https://www.iplt20.com), Twitter/X, Instagram, Facebook, ESPNcricinfo, Cricbuzz, and YouTube |

---

## 🗂️ Data Model

The report is powered by a semantic data model with the following key tables:

| Table | Purpose |
|---|---|
| `ipl_matches_data` | Central fact/measure table — season results, cap holders, boundary counts, and pre-calculated KPI measures |
| `teams_data` | Team dimension table — team names, logos (`image_url`), and points-table stats (matches played/won/lost/tied/no-result, total points) |

### Key Measures & Fields Used

- `Season Winner`, `Season winner Logo`, `Runner Up`, `Runner Up Team Logo`
- `Total Mactches`, `Total Teams`, `Total Venues`, `Total 4's`, `Total 6's`, `Centuries`, `Half Centuries`
- `Orange Cap Holder`, `Orange Cap Runs`, `Orange Cap Team Name`, `Orange Cap Image`
- `PurpleCapHolder`, `PurpleCapWicketCount`, `PurpleCapTeam`, `PurpleCapImage`
- `Top Fours Player Name`, `Top Fours Count`, `Top Fours Player Team Name`
- `Top Six Player Name`, `Top Six Count`, `Top Six Player Team Name`, `Top Six Player Image`
- `Matches Played`, `Matches Won`, `Matches Lost`, `Tie Matches`, `No Result Matches`, `Total Points`
- `season` (slicer field), `IPL Season`

---

## 🛠️ Tech Stack

- **Power BI Desktop** — report authoring and data modeling
- **Power Query (M)** — data cleaning and shaping
- **DAX** — calculated columns and measures
- **Custom visuals used:** Card, Table, Slicer, Shape, Image, Text Box, Action Button

---

## 🚀 Getting Started

### Prerequisites

- [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads) (free) — Windows only
- (Optional) A [Power BI Service](https://app.powerbi.com) account if you want to publish/share the report online

### How to Open

1. Clone or download this repository:
2. Open **`IPL_Dashboard.pbix`** in Power BI Desktop.
3. Use the **Season slicer** at the top-right to explore stats for a specific IPL season.
4. Click the social/media buttons at the bottom-left to jump to official IPL resources.

### Refreshing / Editing Data

The underlying data lives inside the `.pbix` file (imported, not live-connected). To update it:
1. Go to **Home → Transform Data** in Power BI Desktop to open Power Query Editor.
2. Update or point the source query to your latest IPL dataset (season-by-season match results, cap holders, and team standings).
3. Click **Close & Apply**, then **Refresh** to reload the model.


## 📊 Data Source

Match results, points-table figures, and player statistics are sourced from publicly available IPL records (e.g. official IPL website, ESPNcricinfo, Cricbuzz). This project is intended for **educational and analytical purposes only** and is not affiliated with or endorsed by the BCCI, IPL, or Tata Group.

---

## 🙌 Acknowledgements

- IPL branding and imagery belong to their respective owners (BCCI / Tata IPL) and are used here for non-commercial, illustrative purposes.
- Built with ❤️ using Power BI.
