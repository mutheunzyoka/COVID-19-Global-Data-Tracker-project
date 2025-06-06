# COVID-19 Global Data Tracker

## Description

The COVID-19 Global Data Tracker is a data analysis project that explores global COVID-19-related economic indicators, focusing on the cost of living index and its relationships with rent, groceries, and local purchasing power indices. Built using Python and Jupyter Notebook, the project features visualizations (histograms, scatter plots, and kernel density plots) and interactive widgets for dynamic regression analysis and kernel density estimation.

## Dataset

The dataset is sourced from Kaggle: COVID-19 Country Data. It includes the covid19_data - cost_of_living.csv file, which contains economic indices for various countries.

## Objectives
1. Data Acquisition: Download and extract the COVID-19 dataset from Kaggle using the Kaggle API.
   
2.Data Exploration: Analyze the cost of living dataset to understand economic indicators.

3. Visualization: Create histograms, scatter plots, and kernel density plots to identify trends and relationships.



4. Interactive Analysis: Use sliders to adjust regression slopes and kernel density bandwidth for dynamic exploration.

5.Insights Generation: Uncover relationships between cost of living, rent, groceries, and purchasing power.

## Tools and Libraries Used
* Python: Core programming language.
* Pandas: Data manipulation and analysis.
* NumPy: Numerical computations.
* Matplotlib: Plotting histograms and scatter plots.
* Seaborn: Kernel density estimation plots.
* SciPy: Linear regression calculations.
* IPyWidgets: Interactive sliders for visualizations.
* IPympl: Interactive Matplotlib backend.
*Jupyter Notebook: Development and visualization environment.
* Kaggle API: Dataset downloading.
* OS, Shutil, Zipfile: File handling and dataset extraction.

## How to Run/View the Project

### Prerequisites
Install Python 3.x and Jupyter Notebook (e.g., via Anaconda).
Install required libraries:

1. *pip install pandas numpy matplotlib seaborn scipy ipywidgets ipympl jupyterlab kaggle*

2. Upgrade ipywidgets and ipympl for interactive visualizations:
*pip install --upgrade ipywidgets ipympl*

3. Downloads bitsnpieces/covid19-country-data via Kaggle API.
*!pip install kaggle*

4. Runs linear regression for scatter plot trends(scipy)
*!pip install scipy*

5. Enables interactive plots with %matplotlib widget (ipympl)
 *!pip install ipympl*

6. Creates histograms and scatter plots(matplotlib). 
*!pip install --upgrade ipympl matplotlib jupyterlab*

7. Runs notebook, shows visualizations/widgets(jupyterlab)
*!pip install --upgrade ipympl matplotlib jupyterlab*

8. Adds sliders for regression/density adjustments(ipywidgets)
*!pip install ipywidgets, pip install --upgrade ipywidgets*



### Set Up Kaggle API

Download your kaggle.json API key from Kaggle (Account > API > Create New API Token).
Move kaggle.json to the .kaggle directory using Python:

*import os
import shutil
source_path = r"C:\Users\YourUsername\Downloads\kaggle.json"  # Replace with your kaggle.json path
kaggle_dir = os.path.join(os.path.expanduser("~"), ".kaggle")
os.makedirs(kaggle_dir, exist_ok=True)
shutil.move(source_path, os.path.join(kaggle_dir, "kaggle.json"))*

### Download the Dataset

Download the dataset using the Kaggle API:

*kaggle datasets download -d bitsnpieces/covid19-country-data*



### Extract the dataset:

*import zipfile
zip_file_path = "covid19-country-data.zip"
extract_to_path = "covid19-country-data"
with zipfile.ZipFile(zip_file_path, "r") as zip_ref:
    zip_ref.extractall(extract_to_path)*

## Visualizations and Insights
### Histograms:

1.Local Purchasing Power Index: Shows a right-skewed distribution, indicating most countries have moderate to low purchasing power, with few high outliers (e.g., Switzerland).

2.Cost of Living Plus Rent Index: Reveals a spread from low to high costs, with a peak around moderate values, suggesting varied economic conditions globally.

3.Scatter Plots:
Strong positive correlation between Cost of Living and Rent Indices, indicating higher living costs align with higher rents.
Moderate correlation between Purchasing Power and Groceries Indices, with outliers highlighting economic disparities.

4.Interactive Widgets:
Regression Slider: Adjusts regression line slope for Cost of Living vs. Rent, revealing fit quality (R² shown in output).
Kernel Density Bandwidth Slider: Modifies density plot smoothness for Groceries Index, highlighting data distribution nuances.

5.Data Quality: No missing values or duplicates, ensuring reliable analysis.



