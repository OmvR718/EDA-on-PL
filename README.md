# EDA-on-PL
Football Data Analytics &amp; Scraping Toolkit: A Python repository for scraping Premier League stats and analyzing football shot creation, including FPL insights.

# FPL Player Performance Analysis ⚽📊

This project focuses on analyzing football player performance, specifically their Shot-Creating Actions (SCA) and Goal-Creating Actions (GCA). The data is scraped from the web using **Beautiful Soup (`bs4`)** and **`requests`**, and the analysis is performed using Python libraries within a Jupyter Notebook (`FPLAnalysis.ipynb`).

## Project Overview

The primary goal of this project is to gain insights into player performance by:
* Scraping relevant player statistics from football data websites.
* Cleaning and preprocessing the collected data.
* Analyzing key performance indicators such as SCA and GCA.
* Clustering players based on their Shot-Creating Action profiles to identify different player archetypes.

## Dataset

The analysis in `FPLAnalysis.ipynb` uses a dataset named `Shot_Creation.csv`. This dataset contains various player statistics, including:
* Player information (Name, Nation, Position, Age)
* Minutes played (90s)
* Shot-Creating Actions (SCA, SCA90) and their types (PassLive, PassDead, TO, Sh, Fld, Def)
* Goal-Creating Actions (GCA, GCA90) and their types (PassLive.1, PassDead.1, TO.1, Sh.1, Fld.1, Def.1)

The initial data cleaning steps involve dropping the 'Matches' column and removing aggregate rows like 'Squad Total' and 'Opponent Total' to focus on individual player data.

## Analysis and Visualization

The `FPLAnalysis.ipynb` notebook performs the following key analysis steps:
1.  **Data Loading and Cleaning**: Imports necessary libraries (`pandas`, `numpy`) and loads the `Shot_Creation.csv` dataset. It then drops irrelevant columns and filters out summary rows.
2.  **Descriptive Statistics**: Explores the dataset using methods like `.head()`, `.tail()`, and `.describe()`.
3.  **Player Clustering**:
    * Calculates total SCA by summing different types of shot-creating actions.
    * Selects the top 300 players based on their total SCA.
    * Standardizes the SCA features using `StandardScaler` from `scikit-learn`.
    * Applies KMeans clustering to group players into 6 distinct clusters based on their standardized SCA types.
    * Uses Principal Component Analysis (PCA) to reduce the dimensionality of the SCA features to 2 components for visualization.
4.  **Visualization**:
    * Plots the player clusters using `plotly.express` to visualize the distribution of players in a 2D space (PC1 vs. PC2), with players colored by their assigned cluster.

## Technologies Used

* **Data Scraping**:
    * `requests`
    * `bs4` (Beautiful Soup 4)
* **Data Analysis & Manipulation**:
    * `pandas`
    * `numpy`
* **Machine Learning & Dimensionality Reduction**:
    * `scikit-learn` (for `StandardScaler`, `KMeans`, `PCA`)
* **Data Visualization**:
    * `plotly` (`plotly.express`)
    * `matplotlib` (implied by notebook outputs, though not explicitly imported in the provided snippet for clustering visualization)

## How to Run

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd <your-repository-name>
    ```
2.  **Install dependencies:**
    Ensure you have Python installed. You can install the necessary libraries using pip:
    ```bash
    pip install pandas numpy scikit-learn plotly requests beautifulsoup4 jupyter
    ```
3.  **Place the dataset:**
    Make sure the `Shot_Creation.csv` file is in the same directory as the `FPLAnalysis.ipynb` notebook, or update the path in the notebook accordingly.
4.  **Run Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Then, open the `FPLAnalysis.ipynb` file from the Jupyter interface and run the cells.

## Future Work

* Expand the dataset with more seasons or leagues.
* Incorporate more advanced performance metrics.
* Develop interactive dashboards for exploring player clusters and statistics.
* Automate the data scraping and analysis pipeline.

---
##### 📄 License
This project is open-source and available under the Apache License.

