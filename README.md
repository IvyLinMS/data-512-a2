# data-512-a2

This is our second project of Data512 Human-Centered Data Science. Our goal is to explore the concept of bias through data on Wikipedia articles - specifically, articles on political figures from a variety of countries. All analysis are performed in a single Jupyter notebook, named hcds-a2-bias.ipynb.

# Data source:
Wikipedia politicians by country dataset https://figshare.com/articles/dataset/Untitled_Item/5513449
World population data sheet published by the Population Reference Bureau https://docs.google.com/spreadsheets/d/1CFJO2zna2No5KqNm9rPK5PCACoXKzb-nycJFhV689Iw/edit#gid=283125346

# Data processing:
+ Cleaning the Data
+ Get the predicted quality category for each article in the Wikipedia dataset
   + To support easy repro and avoid install the ORES client, use the API call to get the page quality prediction results
   + For page view API data, keep 'access', 'timestamp', 'views' column, update the access type with expected name
+ Combining the Datasets, merge the wikipedia data and population data together use the contry name as key
+ Generating final data file "wp_wpds_politicians_by_country.csv"

# Background information:
ORES is short for "Objective Revision Evaluation Service", it is a machine learning tool that can provide estimates of Wikipedia article quality
The article quality estimates are, from best to worst:
+ FA - Featured article
+ GA - Good article
+ B - B-class article
+ C - C-class article
+ Start - Start-class article
+ Stub - Stub-class article
These were learned based on articles in Wikipedia that were peer-reviewed using the Wikipedia content assessment procedures, refer to https://en.wikipedia.org/wiki/Wikipedia:Content_assessment. These quality classes are a sub-set of quality assessment categories developed by Wikipedia editors

# Data analysis:
Based on the final data csv file from previous step, calculating the proportion (as a percentage) of articles-per-population and high-quality articles for each country AND for each geographic region.

# Data results:
+ Top 10 countries by coverage: 10 highest-ranked countries in terms of number of politician articles as a proportion of country population
+ Bottom 10 countries by coverage: 10 lowest-ranked countries in terms of number of politician articles as a proportion of country population
+ Top 10 countries by relative quality: 10 highest-ranked countries in terms of the relative proportion of politician articles that are of GA and FA-quality
+ Bottom 10 countries by relative quality: 10 lowest-ranked countries in terms of the relative proportion of politician articles that are of GA and FA-quality
+ Geographic regions by coverage: Ranking of geographic regions (in descending order) in terms of the total count of politician articles from countries in each region as a proportion of total regional population
+ Geographic regions by coverage: Ranking of geographic regions (in descending order) in terms of the relative proportion of politician articles from countries in each region that are of GA and FA-quality





