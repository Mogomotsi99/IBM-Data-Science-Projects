# SpaceX Falcon 9 First-Stage Landing Prediction 

## Project Overview
This capstone project analyses SpaceX Falcon 9 launches to investigate factors associated with first-stage landing success. The objective is to use data science and machine learning techniques to predict landing outcomes.

## Objectives
* Collect and explore launch data
* Perform data cleaning and exploratory data analysis
* Investigate relationships between launch features and landing outcomes
* Build and evaluate machine learning classification models
* Summarise findings and their implications

## Repository Structure
* `/SpaceX Data Collection with Webscraping.ipynb`- Automated web scraping utilising **BeautifulSoup** and `requests` to parse the historical Wikipedia directory of Falcon 9 and Falcon Heavy launches, converting unstructured HTML table structures into raw data vectors.
* `/SpaceX Data Wrangling.ipynb`- The structural transformation notebook executing critical clean-up pipelines. Operations include filtering down to Falcon 9 rows exclusively, applying programmatic **mean imputation** to handle missing payload mass inputs, and mathematically deriving a clean binary target column (`Class`: 1 = Successful landing, 0 = Failed landing).
* `/SpaceX Exploratory Data Analysis using SQL.ipynb`- Interactive Jupyter Notebook containing the SQLite database configuration, table schemas, and relational SQL queries (`GROUP BY`, `ORDER BY`, `LIMIT`) used to calculate early program success metrics and baseline flight milestones.
* `/SpaceX Exploratory Data Analysis with Visualisation.ipynb`- Data profiling notebook utilizing **Seaborn** and **Matplotlib** to construct catplots, scatter plots, and bar charts mapping flight trajectories, target orbits, and payload.
* `/SpaceX Interactive Visual Analytics with Folium.ipynb`- Geospatial analysis notebook implementing the **Folium** mapping engine, `MarkerCluster` plugins, and coordinate distance logic (`PolyLine`) to evaluate pad positioning relative to geographic safety hazards.
* `/SpaceX Interactive Dashboard with Plotly Dash.py`- Plotly Dash code script driving the reactive operations dashboard.
* `/SpaceX Machine Learning Prediction.ipynb`- Core machine learning script executing hyperparameter tuning loops using `GridSearchCV`, and comparative confusion matrix evaluations.
* `/SpaceX Capstone Final Presentation.pdf`- Presentation of data-driven insights.

## Core Emprirical Findings
* **Model Accuracy:** Logistic Regression, SVM, and KNN tied with a deployment test set accuracy of **83.33%**.
* **Operational Insights:** First-stage booster recovery correlates heavily with high payload masses (>5,500 kg).
