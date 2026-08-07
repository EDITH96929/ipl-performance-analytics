# 🏏 IPL Player Performance & Match Strategy Analytics

An end-to-end data analytics project that analyzes **17 IPL seasons (2008–2026)** using ball-by-ball data from Cricsheet. The project uncovers player performance across different match phases, venue trends, toss impact, team rivalries, and season-wise scoring patterns through Python-based analysis and an interactive Power BI dashboard.

---

## 📌 Project Overview

This project analyzes:

- **1,243 IPL matches**
- **295,732 ball-by-ball deliveries**
- **17 IPL seasons (2008–2026)**

The analysis focuses on identifying insights that are not visible in traditional scorecards, including:

- Phase-wise batting and bowling performance
- Venue and toss impact
- Team head-to-head records
- Season-wise scoring trends

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python (Pandas, NumPy) | Data cleaning, transformation, and feature engineering |
| Matplotlib & Seaborn | Exploratory Data Analysis (EDA) and visualizations |
| Power BI | Interactive dashboard |
| Jupyter Notebook | Analysis environment |
| Cricsheet | Ball-by-ball IPL dataset |

---

## 📂 Data Source

**Cricsheet** — https://cricsheet.org

Dataset Details:

- IPL Ball-by-Ball CSV
- **1,243 matches**
- **295,732 deliveries**
- **27 columns**, including:
  - Batter
  - Bowler
  - Runs
  - Extras
  - Wicket Type
  - Venue

---

## 📁 Folder Structure

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

---

# 🔧 What Was Built

## 1. Data Cleaning

- Standardized season labels across all IPL seasons
- Unified franchise names (e.g., Delhi Daredevils → Delhi Capitals)
- Filled missing extras with zero values
- Created a Legal Delivery flag by excluding wides and no-balls
- Extracted over numbers and assigned match phases

---

## 2. Feature Engineering

Created several analytical features including:

- **Match Phase**
  - Powerplay (Overs 1–6)
  - Middle Overs (7–15)
  - Death Overs (16–20)

- **Legal Delivery Flag**
- **Bowler Runs Conceded**
- **Match Winner**
- **Result Type**
  - Bat First Win
  - Chase Win

---

## 3. Analysis Performed

### 🏏 Batting Analysis

- Strike Rate by match phase
- Top Powerplay batters
- Best Death-over finishers
- Phase-wise runs and balls faced

### 🎯 Bowling Analysis

- Economy Rate by phase
- Death-over specialists
- Powerplay wicket-takers
- Phase-wise wickets

### 🏟️ Toss & Venue Analysis

- Bat First vs Chase Win %
- Venue-wise winning trends
- Toss impact across venues

### 🤝 Team Head-to-Head

- Win percentage between every team pair
- Match counts
- Dominant rivalries

### 📈 Season Trends

- Average first innings score by season
- Evolution of IPL scoring from 2008–2026

---

# 📊 Key Findings

## 🏏 Batting

- **AB de Villiers** recorded the highest Death Overs Strike Rate (**221.59**) among qualified batters.
- **Rajat Patidar** and **Liam Livingstone** are among the most explosive modern finishers.
- Batting performance varies significantly across match phases, highlighting strong phase specialization.

---

## 🎯 Bowling

- **Lasith Malinga** claimed **122 wickets** in the Death Overs—the highest among qualified bowlers.
- **Sunil Narine** maintained one of the best economy rates across phases.
- **Sohail Tanvir** recorded the lowest Death Overs economy (**6.81**).

---

## 🏟️ Toss & Venue

- Chasing teams won approximately **54%** of IPL matches.
- **MA Chidambaram Stadium (Chepauk)** strongly favors batting first.
- **Sawai Mansingh Stadium (Jaipur)** favors chasing teams.
- UAE venues such as **Sharjah** and **Sheikh Zayed Stadium** also showed a chasing advantage.

---

## 🤝 Team Rivalries

- **Mumbai Indians vs Kolkata Knight Riders**
  - 37 matches
  - MI Win Rate: **67.6%**

- **Chennai Super Kings vs Kolkata Knight Riders**
  - 32 matches
  - CSK Win Rate: **65.6%**

- **Chennai Super Kings vs Royal Challengers Bengaluru**
  - 35 matches
  - CSK Win Rate: **60%**

- **Gujarat Titans vs Rajasthan Royals**
  - GT Win Rate: **72.7%**

---

## 📈 Season Trends

- Average first innings score increased from **161 (2008)** to **193 (2026)**.
- IPL entered a significantly higher-scoring era after **2022**.
- **2009** recorded the lowest average first innings score (**150.3**).

---

# 📊 Power BI Dashboard

The project includes a **4-page interactive Power BI dashboard**.

### Dashboard Pages

1. **Player Analysis**
   - Phase-wise batting
   - Bowling performance
   - Interactive player filters

2. **Team Head-to-Head**
   - Rivalries
   - Win percentages
   - Match counts

3. **Venue & Toss Analysis**
   - Venue impact
   - Toss influence
   - Bat First vs Chase trends

4. **Season Overview**
   - Scoring trends
   - Season comparison
   - Historical analysis

---

# 🚀 How to Run

1. Clone the repository.

```bash
git clone https://github.com/yourusername/ipl-performance-analytics.git
```

2. Download the IPL dataset from **Cricsheet**.

3. Place the CSV file inside:

```text
data/raw/
```

4. Open:

```text
notebooks/ipl_analysis.ipynb
```

5. Run all notebook cells.

6. Processed datasets will be generated in:

```text
data/processed/
```

7. Open:

```text
dashboard/ipl_dashboard.pbix
```

using **Power BI Desktop**.

---

# 👨‍💻 Author

**Sunil Kumar Swain**

🎓 MCA Graduate | Aspiring Data Analyst

- GitHub: https://github.com/EDITH96929
- LinkedIn: https://www.linkedin.com/in/sunil-kumar-swain-584660288
