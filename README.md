# online-shopper-purchase-Behaviour-analysis-using-python
Online Shoppers EDA Project

Exploratory Data Analysis of Online Shoppers’ Purchasing Intention

Description

Many people visit an online shop, but only a few of them buy something. Every visitor who leaves without buying is a lost sale, and 

the money spent to bring that visitor to the site is wasted too. This project studies one year of browsing sessions to find out what

is different between visitors who buy and visitors who do not, and then suggests how the shop can improve its conversion rate.

The data is the Online Shoppers Purchasing Intention Dataset from the UCI Machine Learning Repository. It has 12,330 sessions and 18 columns, 

with numeric columns (page counts, time spent, bounce/exit rates, page value) and categorical columns (month, visitor type, traffic type,

region and more). The target column is Revenue (renamed Purchased in the notebook), which says whether the session ended in a purchase.

Key terms
•Session: one visit of one person to the website.

•Conversion rate: percentage of sessions that end in a purchase.

•Bounce rate: visitors who open one page and leave immediately.

•Exit rate: how often a page is the last page of a visit.

•Page value: average value of the pages a visitor saw before buying.

Project workflow

1.Problem definition and dataset selection: domain is Sales and E-commerce; first look using head, shape, info, 
describe, isnull and duplicated.

2.Data cleaning and pre-processing

◦No missing values or negative durations were found.

◦125 duplicate rows removed (12,330 to 12,205 rows).

◦Columns renamed (for example Revenue to Purchased).

◦True/False converted to 1/0; OS, Browser, Region and Traffic_Type converted to category.

◦New columns created: Total_Pages, Total_Duration, Avg_Time_Per_Page, Season, Engagement (Low / Medium / High / Very High).

◦Skewness checked; outliers kept because they are real heavy-browsing customers; log1p used only to make histograms readable.

◦Cleaned data saved as online_shoppers_cleaned.csv.
3.EDA and visualizations (14 chart cells, 19 visuals)
◦Univariate: purchase outcome, visitor type pie chart, product-page time histogram (log scale), product pages boxplot, sessions per month.
◦Bivariate: conversion by month, by visitor type, page value for buyers vs non-buyers (Mann-Whitney U test), bounce vs exit rate, correlation 
heatmap, special day / weekend / region, conversion by traffic type.
◦Multivariate: month x visitor type pivot heatmap, engagement x visitor type, pairplot.
Key findings
•Only about 15.6% of sessions end in a purchase.
•Page value is the strongest factor: about 56% of sessions with page value above 0 buy, against about 4% when it is 0 (correlation with 
purchase: 0.49).
•New visitors convert more (about 24.9%) than returning visitors (about 14.1%), even though about 85% of visitors are returning.
•November, October and September are the best months. May has the most traffic (about 3,300 sessions) but only about 11% conversion; February
is almost zero (1.7%).
•Higher bounce and exit rates mean fewer purchases; more product pages viewed means more purchases (about 7% for Low engagement vs 26% for Very High).
•Visits close to a special day convert less (3% to 8% vs 16.7% on normal days). Traffic types 1, 3 and 13 bring many visitors but few buyers.
Recommendations
•Push pages with high page value so more sessions reach them.
•Improve landing pages for sources with a high bounce rate.
•Run offers in May and February, and keep stock ready for November.
•Find out why returning visitors buy less and try loyalty offers.
•Review the budget spent on traffic types 1, 3 and 13.
Limitations
•Data covers only one year; January and April are missing.
•Region, Browser and Traffic Type are anonymous codes.
•Each row is one session, not one customer.
•Correlation does not prove that a factor causes buying.
Getting Started
Dependencies
•Python 3.8 or higher
•Jupyter Notebook or JupyterLab
•Libraries:
◦pandas
◦numpy
◦matplotlib
◦seaborn
◦scipy
•Any OS that runs Python (for example Windows 10 or later, macOS, Linux)
Installing
•Download or clone this repository and keep all the files in the same folder:
Online_Shoppers_EDA_Project.ipynb
online_shoppers_intention.csv
README.md
•The raw dataset can also be downloaded from the UCI Machine Learning Repository (Online Shoppers Purchasing Intention Dataset).
•Install the required libraries:
pip install pandas numpy matplotlib seaborn scipy notebook
•No changes to the files are needed. The notebook reads online_shoppers_intention.csv from the same folder.
Executing program
•Open a terminal in the project folder and start Jupyter:
jupyter notebook
•Open Online_Shoppers_EDA_Project.ipynb.
•Run the cells from top to bottom (Kernel > Restart & Run All), in this order:
◦Import libraries and load the data
◦Initial EDA (shape, info, describe, missing values, duplicates)
◦Data cleaning and pre-processing
◦Univariate, bivariate and multivariate analysis
◦Save the cleaned data
•After the last cell, online_shoppers_cleaned.csv is created in the same folder.
Help
•FileNotFoundError for the CSV: make sure online_shoppers_intention.csv is in the same folder as the notebook, or Jupyter
was started from that folder.
•ModuleNotFoundError: install the missing library with pip install <library-name>.
•Charts not showing: run %matplotlib inline in a cell above the charts.
•Different numbers than in the report: run all cells in order, because the duplicate removal and new columns are used by later cells.
pip install --upgrade pandas numpy matplotlib seaborn scipy
Authors
Priyanka R
Version History
•0.1
◦Initial Release: data cleaning, 14 chart cells (19 visuals), insights and recommendations
License
This project is licensed under the [MIT] License - see the LICENSE.md file for details
Acknowledgments
•Dataset: Sakar, C.O., Polat, S.O., Katircioglu, M. et al. Online Shoppers Purchasing Intention Dataset, UCI Machine Learning Repository
•awesome-readme
•PurpleBooth
•dbader
•zenorocha
•fvcproductions
