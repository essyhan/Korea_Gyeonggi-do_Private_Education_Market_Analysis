# 🏫 South Korean Education Market Analysis & Regional Clustering

## 📌 Project Overview
This project provides a comprehensive statistical analysis and machine learning clustering of the private education market (Academies/Hagwons) in South Korea . The goal is to uncover regional educational disparities, analyze tuition fee trends, and segment cities based on their distinct educational infrastructure . 

## 🛠️ Tech Stack & Methodology
* **Language:** `R` 
* **Libraries:** `dplyr`, `ggplot2`, `stringr`, `factoextra`, `tidyverse` 
* **Data Wrangling & Text Mining:** 
  * Imputed missing categorical values (e.g., specific subjects and founder names) by employing Regular Expressions (Regex) and text mining on academy names .
  * Standardized diverse pricing structures into a unified `monthly_fee` metric and categorized hundreds of courses into 16 simplified fields .
* **Statistical Analysis:** Conducted Pearson correlation and linear regression to evaluate the relationship between regional population density, Net Academy Ratio (NAR), and average monthly fees .
* **Machine Learning (Clustering):**
  * Performed **K-Means Clustering** to group regions based on their academy type distributions . 
  * Determined the optimal number of clusters (`k=3`) using the Silhouette Coefficient method .
  * Utilized **Principal Component Analysis (PCA)** to visualize high-dimensional clustering results and interpret the underlying variance .

## 💡 Key Insights
* **Regional Segmentation:** The K-Means model effectively categorized cities into 3 distinct tiers. Notably, the city of Echeon formed its own unique cluster due to an unusually high ratio of art-related academies compared to cities of similar population size like Paju .
* **Market Dynamics:** Discovered statistically significant correlations between the average number of instructors per academy and regional monthly tuition fees .

## 🙋‍♀️ My Role
As a core contributor to this data science project (Group 6), I focused heavily on ensuring data integrity through programmatic text manipulation and architecting the unsupervised learning pipeline to derive actionable demographic insights .
