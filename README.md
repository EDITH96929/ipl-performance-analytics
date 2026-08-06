### 🏏 IPL Player Performance & Match Strategy Analytics

## Project Overview
Analysis of 17 seasons of IPL ball-by-ball data (2008–2026) covering 1,243 matches and 295,732 deliveries. The goal was to uncover phase-specific player strengths, venue patterns, toss impact, and team rivalry trends that are not visible in standard scorecards.

---

## Tech Stack
| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data cleaning, wrangling, feature engineering |
| Matplotlib, Seaborn | Exploratory data analysis, visualisations |
| Power BI | Interactive 4-page dashboard |
| Jupyter Notebook | Analysis environment |
| Cricsheet | Data source (ball-by-ball CSVs) |

---

## Data Source
**Cricsheet** — cricsheet.org  
- Dataset: IPL CSV (all_matches.csv)  
- 1,243 matches across 17 seasons (2008–2026)  
- 295,732 ball-by-ball delivery records  
- 27 columns including striker, bowler, runs, extras, wicket type, venue

---
## Folder Structure

```text
ipl-performance-analytics/
│
├── data/
│   ├── raw/
│   │   └── all_matches.csv
│   └── processed/
│       ├── batting_phase_stats.csv
│       ├── bowling_phase_stats.csv
│       ├── toss_venue_analysis.csv
│       ├── team_head_to_head.csv
│       ├── season_scoring_trend.csv
│       └── match_summary.csv
│
├── notebooks/
│   └── ipl_analysis.ipynb
│
├── dashboard/
│   └── ipl_dashboard.pbix
│
└── README.md
```
```

## What Was Built

### 1. Data Cleaning
- Standardised 18 season labels (mixed integer and string formats)
- Unified franchise names across eras (Delhi Daredevils → Delhi Capitals, RCB name fix etc.)
- Filled missing extras columns with 0
- Flagged legal deliveries (excluding wides and no-balls) for accurate batting and bowling metrics
- Extracted over number from ball column and created match phase labels

### 2. Feature Engineering
- **Match Phase** — Powerplay (overs 1–6), Middle (7–15), Death (16–20)
- **Legal Delivery Flag** — used for correct strike rate and economy calculations
- **Bowler Runs** — runs off bat + wides + no-balls charged to bowler
- **Match Winner** — derived from first and second innings totals
- **Result Type** — Bat First Win vs Chase Win per match

### 3. Analysis Areas

#### Batting
- Strike rate by phase per batsman (minimum 50 legal balls)
- Top death over hitters and powerplay anchors
- Phase-wise runs and balls faced breakdown

#### Bowling  
- Economy rate by phase per bowler (minimum 60 legal balls)
- Death over specialists and powerplay wicket takers
- Wickets per phase analysis

#### Toss & Venue
- Overall IPL bat first win % vs chase win %
- Venue-wise bat first win % (minimum 10 matches per venue)
- Identified venues heavily favouring batting first vs chasing

#### Team Head to Head
- Win % for every team pair with minimum 8 matches
- Identified dominant teams in key rivalries

#### Season Trends
- Average first innings score per season (2008–2026)
- Scoring evolution across IPL eras

---

## Key Findings

### Batting
- **AB de Villiers** leads death over batting with 221.59 SR (829 balls — large sample)
- **RM Patidar** and **LS Livingstone** are the standout modern death hitters
- Death over SR varies massively across batters — phase specialisation is real

### Bowling
- **SL Malinga** took 122 death wickets — most among qualified death bowlers
- **SP Narine** is the most economical spinner across phases with 7.25 death economy
- **Sohail Tanvir** has the lowest death economy (6.81) among qualified bowlers

### Toss & Venue
- Overall chasing is slightly favoured in IPL — 54% chase win rate
- **Chepauk (Chennai)** is the strongest batting-first venue at 62.5% win rate
- **Sawai Mansingh Stadium (Jaipur)** heavily favours chasing — only 31.9% bat first win rate
- **Sharjah** and **Sheikh Zayed** (UAE venues) strongly favour chasing

### Team Rivalries
- **Mumbai Indians vs KKR** is the most played rivalry — 37 matches, MI leads 67.6%
- **CSK vs KKR** — 32 matches, CSK wins 65.6%
- **CSK vs RCB** — 35 matches, CSK wins 60%
- **Gujarat Titans vs Rajasthan Royals** — GT dominates with 72.7% win rate
- CSK appears in the most dominant rivalry positions overall

### Season Trends
- Average first innings score grew from **161 (2008)** to **193 (2026)**
- Significant scoring jump from 2022 onwards — modern IPL is a higher scoring era
- 2009 was the lowest scoring season on average (150.3)

---

## Dashboard (Power BI)
4-page interactive dashboard built in Power BI Desktop:
- **Page 1 — Player Analysis** — Phase-wise batting and bowling stats with slicers
- **Page 2 — Team Head to Head** — Rivalry win % and match counts
- **Page 3 — Venue & Toss** — Venue impact on match results
- **Page 4 — Season Overview** — Scoring trends across 17 seasons

---

## How to Run

1. Clone this repository
2. Download IPL CSV data from cricsheet.org/matches and place in `data/raw/`
3. Open `notebooks/ipl_analysis.ipynb` in Jupyter Notebook
4. Run all cells in order
5. Exported CSVs will appear in `data/processed/`
6. Open `dashboard/ipl_dashboard.pbix` in Power BI Desktop

---

## Author
**Sunil Kumar Swain**  
MCA Graduate | Aspiring Data Analyst  
GitHub: github.com/EDITH96929  
LinkedIn: linkedin.com/in/sunil-kumar-swain-584660288
