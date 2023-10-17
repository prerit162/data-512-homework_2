# AIM

The goal of this assignment is to explore the concept of bias in data using Wikipedia articles about cities in different US states.

# Folder Hierarchy

├── Data/<br>
│   ├── thank_the_academy.AUG.2023.csv.xlsx<br>
├── Code/<br>
│   └── Analysis.ipynb<br>
└── Output/<br>
&emsp; ├── academy_monthly_cumulative_201507-202309.json<br>
&emsp; ├── academy_monthly_mobile_201507-202309.json<br>
&emsp; └── academy_monthly_desktop_201507-202309.json<br>
&emsp; └── Fewest10_plot.png<br>
&emsp; └── Max_Min_plot.png<br>
&emsp; └── Top10_plot.png<br>


# Data Sources and Description

The Wikipedia Category:Lists of cities in the United States by state - us_cities_by_state_SEPT.2023.csv

The US Census Bureau provides updated population estimates for every US state - Population.xlsx

List of regions of the United States by the US Census Bureau - US States by Region - US Census Bureau.xlsx

Objective Revision Evaluation Service - A machine learning tool that can provide estimates of Wikipedia article quality. The article quality estimates are, from best to worst:
FA - Featured article
GA - Good article (sometimes called A-class)
B - B-class article
C - C-class article
Start - Start-class article
Stub - Stub-class article

# API documentation

[API Documentation](https://www.mediawiki.org/wiki/API:Info)

[API Documentation](https://www.mediawiki.org/wiki/API:Main_page)

[LiftWing documentation](https://wikitech.wikimedia.org/wiki/Machine_Learning/LiftWing)

[ORES API documentation](https://ores.wikimedia.org/docs)

[ORES LiftWing documentation](https://wikitech.wikimedia.org/wiki/Machine_Learning/LiftWing/Usage)

# Code
[Reference Code for API call](https://drive.google.com/file/d/1XjFhd3eXx704tcdfQ4Q1OQn0LWKCRNJm/view)

[License](https://creativecommons.org/licenses/by/4.0/)


# Output

wp_scored_city_articles_by_state.csv

The file is of the following schema which contains merged data from all the data sources:

Columns : <b> state , <b> regional_division, <b> population, <b> article_title , <b>revision_id , <b>article_quality



# License

This assignment code is released under the MIT License.

# Reflection and Addressing Questions

What biases did you expect to find in the data (before you started working with it), and why?

What (potential) sources of bias did you discover in the course of your data processing and analysis?

What might your results suggest about (English) Wikipedia as a data source?

Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?

Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?

How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?

