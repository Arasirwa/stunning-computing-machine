# 📽️ Movie Studio Case Analysis
## 📊 Overview
This project analyzes multiple movie databases to support strategic decision-making for a company entering the movie production industry. The goal is to find out the safest and risk-free way to break into the movie scene based on metadata from previously released movies

## 🧠 Business Problem
> Your company now sees all the big companies creating original video content, and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of your company's new movie studio can use to help decide what type of films to create.
> 
## ❔Key Question Answered
* Which genres are the most profitable?
* What budget range optimizes return on investment (ROI)?
* When should we release films for maximum financial gain?

## 📁 Dataset
The following five datasets were used:
* [Internet Movie Database (IMDb)](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [The Movie Database (TMDb)](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)
* [Box Office Mojo](https://www.boxofficemojo.com/)

## ✅ Business Recommendations
1. Start with Animation, Adventure, and Comedy genres as they appease a wide population and offer the greatest profit and ROI margins.
2. A production budget of $ 1 million and $ 10 million is enough.
3. Focus on releasing movies for the worldwide market rather than for the domestic market to generate greater profit margins.
4. Focus on releasing and showcasing during the summer for maximum financial returns and Fridays for optimal weekend performance.
5. Maintain a runtime of 90 -120 minutes for commercial viability.

## ⚙️ Tools Used
- Python: Data cleaning, preprocessing, exploratory analysis, and hypothesis testing (Pandas, Matplotlib, Seaborn, Scipy)

## 💻 Getting Started

To explore or replicate this analysis locally, follow the steps below:

### 1. 📦 Clone the Repository

```bash
git clone git@github.com:Arasirwa/stunning-computing-machine.git
cd stunning-computing-machine
```

### 2. 🐍 Set Up Your Conda Environment

Make sure you have [Anaconda](https://www.anaconda.com/) installed. Then run:

```bash
conda create --stunning-computing-machine python=3.10
conda activate stunning-computing-machine
```

### 3. 📚 Install Required Packages

You can install the required Python libraries using:

```bash
pip install pandas numpy matplotlib seaborn scipy
```

### 4. 📁 Load the Dataset

Ensure the dataset is organized in the following folder structure:

```
Data/
└── bom.movie_gross.csv.gz/
└── im.db.zip
└── rt.movie_info.tsv.gz
└── rt.reviews.tsv.gz
└── tmdb.movies.csv.gz
└── tn.movie_budgets.csv.gz
```

Then, in your Python script or notebook, load the data using:

```python
import pandas as pd
import sqlite3

#-------going through SQl-----#
def load_tables(connection):
    table_names = pd.read_sql(
        "SELECT name FROM sqlite_master WHERE type='table';", connection
    )["name"].tolist()
    sql_tables = {
        table_name: pd.read_sql(f"SELECT * FROM {table_name}", connection)
        for table_name in table_names
    }
    return sql_tables

path = '../Data/im.db'
conn = sqlite3.connect(path)

imdb_tables = load_tables(conn)

print(imdb_tables.keys())

#-------CSV and TSV Data ------#

bom_movie = pd.read_csv("../Data/bom.movie_gross.csv")
rt_info = pd.read_csv("../Data/rt.movie_info.tsv", sep='\t', encoding='latin1')
rt_reviews = pd.read_csv("../Data/rt.reviews.tsv", sep='\t', encoding='latin1')
tmdb_df = pd.read_csv("../Data/tmdb.movies.csv")
tn_budget = pd.read_csv("../Data/tn.movie_budgets.csv")
```
---
## 🫱🏽‍🫲🏽 Acknowledgements
Special thanks to the following datasets for making this project possible
* [Internet Movie Database (IMDb)](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [The Movie Database (TMDb)](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)
* [Box Office Mojo](https://www.boxofficemojo.com/)
