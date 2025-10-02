# ⚽ Euro Football Analytics

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Latest-green.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.0+-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

**Comprehensive data analysis and visualization of Europe's Top 5 football leagues**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Visualizations](#-visualizations) • [Contributing](#-contributing)

</div>

---

## 📊 Overview

Euro Football Analytics is a powerful Python toolkit for analyzing player performance across Europe's elite football competitions. Dive deep into the 2024/25 season statistics from the **Premier League**, **La Liga**, **Serie A**, **Bundesliga**, and **Ligue 1**.

Whether you're a data scientist, football analyst, fantasy football enthusiast, or sports journalist, this project provides the tools to transform raw statistics into actionable insights through beautiful, publication-ready visualizations.

## ✨ Features

### 🏆 Team Analysis
- **Comprehensive Statistics**: Query any team to view complete player performance metrics
- **Sortable DataFrames**: Automatically organized by Goals + Assists (G+A)
- **Performance Breakdown**: Individual player goals, assists, positions, and age data
- **Team Totals**: Aggregate statistics with automatic calculation of team-wide metrics

### 🎯 Top Scorers Analysis
- **Cross-League Rankings**: Identify Europe's top 20 (or more) goal scorers
- **League Comparisons**: Compare scoring distributions across all 5 leagues
- **Goals vs Assists**: Analyze the relationship between scoring and playmaking abilities
- **Flexible Filtering**: Customize the number of top players to display

### 📈 Professional Visualizations
- **KDE Density Plots**: Beautiful heatmap-style distributions showing goals vs assists patterns
- **Color-Coded Charts**: League-specific color branding for easy identification
- **Multi-Panel Dashboards**: Comprehensive 4-plot layouts combining multiple analytical perspectives
- **Modern Design**: Clean, elegant visualizations ready for presentations and reports

## 🛠️ Technologies

- **Python 3.8+**
- **Pandas** - Data manipulation and analysis
- **Matplotlib** - Core visualization library
- **Seaborn** - Statistical data visualization and KDE plots
- **NumPy** - Numerical computations

## 📦 Installation

### Prerequisites
```bash
python --version  # Ensure Python 3.8 or higher
```

### Clone the Repository
```bash
git clone https://github.com/yourusername/euro-football-analytics.git
cd euro-football-analytics
```

### Install Dependencies
```bash
pip install pandas matplotlib seaborn numpy
```

Or using requirements.txt:
```bash
pip install -r requirements.txt
```

## 🚀 Usage

### Quick Start

```python
import pandas as pd
from football_analytics import Team_Stats, plot_team_stats, plot_top_scorers_europe

# Load your dataset
df = pd.read_csv('data/player_stats_2024_25.csv')

# Analyze a specific team
arsenal_stats = Team_Stats(df, 'Arsenal')
print(arsenal_stats)

# Visualize team performance
plot_team_stats(df, 'Manchester City')

# View top scorers across Europe
top_scorers = plot_top_scorers_europe(df, top_n=20)
```

### Function Reference

#### `Team_Stats(df, team=None)`
Generate comprehensive team statistics DataFrame.

**Parameters:**
- `df`: DataFrame containing player data
- `team`: Team name (string). If None, prompts user for input

**Returns:** DataFrame with player statistics including totals row

#### `plot_team_stats(df, team=None)`
Create 4-panel visualization for team analysis.

**Plots include:**
- Top 10 players by G+A (horizontal bar chart)
- Goals vs Assists KDE distribution
- Goals vs Assists breakdown
- Team summary statistics

#### `plot_top_scorers_europe(df, top_n=20)`
Visualize top goal scorers across Europe's top 5 leagues.

**Parameters:**
- `df`: DataFrame containing player data
- `top_n`: Number of top scorers to display (default: 20)

**Returns:** DataFrame of top scorers

## 📊 Visualizations

### Team Analysis Dashboard
<div align="center">
<img src="assets/team_analysis_example.png" alt="Team Analysis" width="800"/>
</div>

Features color-coded player rankings, KDE distributions, and comprehensive statistics.

### Top Scorers Across Europe
<div align="center">
<img src="assets/top_scorers_example.png" alt="Top Scorers" width="800"/>
</div>

Beautiful 4-panel visualization showcasing Europe's elite goal scorers with league-specific branding.

## 📁 Project Structure

```
euro-football-analytics/
│
├── data/
│   └── player_stats_2024_25.csv
│
├── src/
│   ├── football_analytics.py
│   ├── team_stats.py
│   └── visualizations.py
│
├── notebooks/
│   └── analysis.ipynb
│
├── assets/
│   └── (visualization examples)
│
├── requirements.txt
├── README.md
└── LICENSE
```

## 📋 Data Structure

Your CSV file should contain the following columns:

| Column | Description |
|--------|-------------|
| `Squad` | Team name |
| `Player` | Player name |
| `Nation` | League identifier (e.g., "eng ENG" for Premier League) |
| `Pos` | Playing position |
| `Age` | Player age |
| `Gls` | Goals scored |
| `Ast` | Assists |
| `G+A` | Combined goals and assists |

## 🏆 Supported Leagues

| League | Country | Identifier |
|--------|---------|------------|
| 🏴󠁧󠁢󠁥󠁮󠁧󠁿 Premier League | England | `eng ENG` |
| 🇪🇸 La Liga | Spain | `es ESP` |
| 🇮🇹 Serie A | Italy | `it ITA` |
| 🇩🇪 Bundesliga | Germany | `de GER` |
| 🇫🇷 Ligue 1 | France | `fr FRA` |

## 💡 Use Cases

- **🔍 Scouting**: Identify top performers across leagues for recruitment
- **📊 Performance Analysis**: Compare players and teams statistically
- **📰 Data Journalism**: Create compelling football analytics stories
- **🎮 Fantasy Football**: Make data-driven player selections
- **🎓 Academic Research**: Football statistics and performance studies
- **📱 Social Media**: Generate shareable infographics and insights

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contributions
- Add more league support
- Implement player comparison features
- Create interactive dashboards
- Add historical season analysis
- Develop predictive models

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Data sourced from official league statistics
- Inspired by modern football analytics and data visualization best practices
- Built with passion for football and data science

## 📬 Contact

**Your Name**
- GitHub: [@yourusername](https://github.com/SoulaymaneBoulaich)
- Email: soulaymaneboulaich@gmail.com
- Twitter: [@yourlinkedin](https://www.linkedin.com/in/soulaymane-boulaich-b08ba532b/)

## ⭐ Show Your Support

Give a ⭐️ if this project helped you!

---

<div align="center">

**Made with ❤️ and ⚽ by SOulaymane**

[⬆ Back to Top](#-euro-football-analytics)

</div>
