# EDA-on-PL: Premier League Football Data Analytics & Shot Creation Analysis

A Python toolkit for advanced analysis of Premier League player creativity, tactical flexibility, and shot/goal creation, with actionable insights for FPL (Fantasy Premier League) and football analytics.

## 📊 Features
- **Comprehensive Data Cleaning:** Handles raw FPL and shot creation datasets, removing aggregates and standardizing columns.
- **Advanced Analytics:**
  - Calculates take-on dependency ratios, SCA90/GCA90 rankings, and composite efficiency scores.
  - Visualizes SCA90 vs take-on dependency (interactive scatter plot, colored by position, sized by age).
  - Performs robust statistical testing (ANOVA, Kruskal-Wallis) for position and age effects.
  - Bins players by age, analyzes age-related trends, and identifies peak creative years with polynomial regression.
  - Computes SCA→GCA conversion efficiency and visualizes age curves.
- **Tactical Flexibility Indices:**
  - Develops and refines SCA_flex and GCA_flex indices using weighted Shannon entropy with tactical weights and a log-based volume boost for high-volume players.
  - Dual flexibility ranking and quadrant analysis to identify tactical archetypes (e.g., versatile, specialist, build-up/final ball flexibility).
  - Position-specific flexibility benchmarks for player evaluation.
- **Unsupervised Clustering:**
  - Clusters players by detailed shot/goal creation breakdowns using K-means and t-SNE.
  - Assigns unique creativity archetypes (Set-piece Specialists, Take-on Creators, Hybrid Creators) to clusters.
  - Provides real player examples for each archetype.
- **Web Scraping:**
  - Scrapes player/team stats from FBref.com using BeautifulSoup and requests (see `FPP.py`).

## 🛠️ Requirements
- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- scikit-learn
- requests
- beautifulsoup4

## 📂 Files
- `FPLAnalysis.ipynb`: Jupyter notebook for data cleaning, EDA, tactical flexibility, clustering, and visualization.
- `Shot_Creation.csv`: Input dataset (included in the repo).
- `FPP.py`: Script to scrape football statistics from FBref using BeautifulSoup.

## 🚀 Usage
1. Clone the repository and install requirements:
   ```bash
   pip install -r requirements.txt
   ```
2. Open `FPLAnalysis.ipynb` in Jupyter or VS Code and run all cells.
3. (Optional) Use `FPP.py` to scrape new data from FBref.com.

## 📈 Example Analyses
- Identify the most efficient creators in the Premier League.
- Visualize and compare creative output by position and age.
- Discover player archetypes and see real examples for each creative style.
- Benchmark tactical flexibility by position and creation type.
- Use dual flexibility ranking and quadrant analysis to identify versatile and specialist creators.

## 📄 License
This project is open-source and available under the MIT License.

