## Canopy French-Language Movie Analysis — Data Pipeline, EDA & Visualization Project
**Python • Pandas • Matplotlib • Seaborn • Bokeh • Data Wrangling • Genre Modelling • Visual Insights**



-- Project Overview

This project analyzes French-language movies to support Canopy, a streaming platform aiming to differentiate itself by offering diverse, high-quality French cinema.

The project applies:

Systematic data cleaning

Data wrangling & merging

Genre modelling

Exploratory visualizations

Trend analysis

Runtime & rating analysis

Age-appropriateness insights

The goal is to help Canopy build a smarter, data-driven content strategy for French films.

- Dataset Summary

The dataset (from Netflix-style movie listings) includes:

Title

Year

Age Group

IMDb Rating

Rotten Tomatoes Score

Directors

Genres

Country

Language

Runtime

As shown on page 3 of report → the .info(), .head(), and dtype outputs confirm structure and missing values.


 1. Data Analysis Approach (CRISP-style)
✔ 1.1 Data Loading

Data was loaded using Pandas, with verification using:

shape

info()

head()

columns

(Shown on page 3 of the report) →

✔ 1.2 Initial Inspection

Critical columns identified for Canopy analysis:

Title

Age

IMDb

Genres

Language

Runtime

This helped define which attributes would fuel insights on movie quality & audience fit.

 2. Data Wrangling & Cleaning
✔ Filtering for French-language films

All movies with non-French languages removed.
(Page 4) →

✔ Handling Missing Values

Dropped missing Language and IMDb rows, because they are critical.

Kept missing Age & Genre temporarily to avoid losing French content.

✔ Removing Duplicates

Duplicates removed based on Title.
(Page 4) →

✔ Dataset Shape After Cleaning

Reduced to 1,491 rows of valid French-language movies.

 3. Genre Modelling & Transformation

Genres often contain multiple values, e.g.:
Action, Adventure, Romance

To analyze them properly:

✔ Split genre strings into multiple rows

Using .str.split(',') and .explode()
(Page 6) →

✔ Genre Frequency Findings

After expanding genres:

Genre	Count
Drama	386
Comedy	147
Thriller	147
Romance	135
Documentary	86
Action	92
Horror	39
Fantasy	49
Sport	10

 Drama is dominant, while Sport & Musical are rare niches that Canopy could develop.

 4. Exploratory Data Visualizations (EDA)

All visualisations were created using Matplotlib, Seaborn, and Bokeh.

 4.1 Average Runtime Analysis

(See the bar chart on page 7 of the report) →

Key insight:

French Movies Runtime ≈ 101.5 min

All Movies Runtime ≈ 94 min

  French films tend to be longer — aligning with the finding that movies of 90–120 min perform best (page 11).

 4.2 Average IMDb Rating

(Bar chart on page 9) →

French movies IMDb avg = 6.34

All movies IMDb avg = 5.90

 French films perform slightly better than the global average.

 4.3 Scatter Plot — Year vs IMDb Rating

(Scatter plot on page 9) →

Insights:

Older movies show wider rating spread.

Recent films cluster around mid-range IMDb scores.

Some eras consistently produce high-rated films.

 Canopy can target iconic decades with higher audience appeal.

 4.4 Runtime vs IMDb Rating (Trend Analysis)

The scatter plot on page 11 indicates:

✔ Optimal runtime range for highly rated films:

90–120 minutes

 Canopy should prioritize films in this runtime window.

 5. Conclusions & Insights
 The strongest insights from the project:
 French movies outperform average films

IMDb ≈ 6.34 vs 5.90 globally

Longer runtimes, but still within preferred ranges

 Genres are diverse — but dominated by Drama

Opportunity to expand Sport, Musical, Animation categories

Dual-genre films (Drama + Romance) are most common

 Runtime directly influences ratings

Movies between 90–120 minutes scored highest.

 Ideal content strategy includes:

Family-friendly films

Teen content

High-rated films from specific high-performing decades

Underrepresented genres to stand out in the market

 6. Recommendations for Canopy
✔ Expand family & teen categories

(Page 11–12) →

✔ Prioritize films within 90–120 min

This aligns with highest IMDb scores.

✔ Build a balanced genre catalogue

Combine high-volume genres (Drama/Comedy) with niche (Musical/Sport).

✔ Use data continuously

Monitor viewership patterns & ratings using dashboards.

✔ Ethical Content Practices

(Page 12) →

Ensure cultural diversity

Protect data privacy (GDPR-aligned)

Avoid exploitation of user behavior data
