# Korea_Gyeonggi-do_Private_Education_Market_Analysis
This project explores the landscape of private educations (Hagwons) in Gyeonggi-do to uncover market trends, tuition fee drivers, and regional characteristics.
# Gyeonggi-do Private Academy Market Analysis

## 📌 Overview
This project explores the landscape of private academies (Hagwons) in Gyeonggi-do to uncover market trends, tuition fee drivers, and regional characteristics. By analyzing a large-scale dataset, this project identifies the socio-economic and demographic factors that influence the private education market, providing data-driven insights into regional educational infrastructure.

## 📊 Dataset
* **Source:** Gyeonggi-do private academy general information.
* **Supplementary Data:** Gyeonggi-do Population and Area data (from Gyeonggi-do data dream portal).
* **Size:** 232,989 records and 21 initial variables.
* **Refinement:** The dataset was pre-processed and refined to 13 highly relevant variables for deep analysis.

## 🛠️ Methodology & Data Pre-processing
 To ensure accurate analysis, the raw data underwent rigorous cleaning, conversion, and simplification:
1.   **Data Cleaning:** Removed irrelevant categories such as "Adult Education" and "Reading Room" to focus strictly on elementary, middle, and high school student facilities.  Resolved missing values based on row context.
2.   **Data Simplification:** Standardized column names and grouped fragmented subject values into unified, simple categories (e.g., grouping various art classes under "Arts"). 
3.   **Feature Engineering:** Created new analytical columns, including the number of students per instructor and simplified monthly tuition fees.  Calculated a custom metric, `NAR` (Number of Academies per Region relative to middle/high schools), to gauge local market saturation.

## 🔍 Key Findings (EDA)
Our Exploratory Data Analysis yielded several critical insights into the education market:
*  **Population & Academy Density:** There is a significant positive correlation (Pearson correlation: 0.46) between regional population density and the NAR value.  As population density increases, the concentration of academies relative to traditional schools also increases.
*  **Tuition Fee Drivers:** We tested the hypothesis that larger academy capacities would lower tuition fees, which proved false.  Instead, a strong positive correlation exists between the average number of instructors and the average monthly tuition fee (p-value: 1.07e-06). 
*  **Subject Correlations:** The correlation between different types of academies (e.g., Science and College-Prep) is heavily influenced by the primary age group of the student base rather than just the subject matter itself.

## 🤖 Machine Learning: Regional Clustering
 To categorize regional education markets, we applied **Principal Component Analysis (PCA)** and **K-Means Clustering**.
*  **Variables Used:** Regional capacity averages, student-per-instructor ratios, and class subject ratios.
*  **Optimization:** Using the average silhouette width method, we identified **K=3** as the optimal number of clusters.
*  **Results:** The clustering successfully segmented the regions into three distinct profiles (groups of 21 cities, 7 cities, and 1 isolated city—Icheon), driven primarily by the proportion of art classes relative to total academies.

## 💡 Challenges Overcome
*  Navigated the uncertainty and inconsistency of raw course classification criteria.
*  Successfully merged disparate datasets (academy info, school info, population density) to find statistically meaningful relationships.

## 💻 Technologies Used
*  **Language:** R
*  **Techniques:** Data Wrangling, Exploratory Data Analysis (EDA), Hypothesis Testing, Principal Component Analysis (PCA), K-Means Clustering.
