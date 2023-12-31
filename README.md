# AIM

The goal of this assignment is to explore the concept of bias in data using Wikipedia articles about cities in different US states.

# Folder Hierarchy

├── <b>Data/</b><br>
&nbsp;&nbsp;&nbsp;├── Population.xlsx<br>
&nbsp;&nbsp;&nbsp;├── US States by Region - US Census Bureau.xlsx<br>
&nbsp;&nbsp;&nbsp;├── Wiki_Scraped_data.csv<br>
&nbsp;&nbsp;&nbsp;├── ores_score.csv<br>
&nbsp;&nbsp;&nbsp;├── us_cities_by_state_SEPT.2023.csv<br>
├── <b>Code/</b><br>
&nbsp;&nbsp;&nbsp;├── Analysis.ipynb<br>
├── <b>Output/</b><br>
&nbsp;&nbsp;&nbsp;├── wp_scored_city_articles_by_state.csv<br>
&nbsp;&nbsp;&nbsp;├── Analysis_1.png<br>
&nbsp;&nbsp;&nbsp;├── Analysis_2.png<br>
&nbsp;&nbsp;&nbsp;├── Analysis_3.png<br>
&nbsp;&nbsp;&nbsp;├── Analysis_4.png<br>
&nbsp;&nbsp;&nbsp;├── Analysis_5.png<br>
&nbsp;&nbsp;&nbsp;├── Analysis_6.png<br>

# Prerequisites
Before using this code, ensure you have the following prerequisites installed:

1.) Python 3

2.) Requests

3.) Pandas

# Reproducibility

The following steps need to followed to run this code seamlessly :

&emsp; Clone this repository to your local machine.<br>
&emsp; Install all the required libraries.<br>
&emsp; Run Analysis.ipynb to generate all Analysis Tables and output csv file<br>


# Data Sources and Description

<b>us_cities_by_state_SEPT.2023.csv </b> - The Wikipedia Category:Lists of cities in the United States by state

<b>Population.xlsx </b> -The US Census Bureau population estimates for every US state

<b>US States by Region - US Census Bureau.xlsx </b> - List of regions of the United States by the US Census Bureau 

<b> Objective Revision Evaluation Service - A machine learning tool that can provide estimates of Wikipedia article quality. The article quality estimates are, from best to worst:</b>

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

# Licenses and Reference Code

This project is licensed under the MIT License.

[Reference Code for MediaWiki API](https://colab.research.google.com/drive/15UoE16s-IccCTOXREjU3xDIz07tlpyrl)

[Reference Code for ORES API](https://colab.research.google.com/drive/17C9xsmR9U3lJeD52UTbAedlHDetwYsxs#scrollTo=GgcjNS0j2VSQ)

[Creative Commons License](https://creativecommons.org/licenses/by/4.0/)

[Wikimedia Foundation REST API](https://www.mediawiki.org/wiki/API:REST_API#Terms_and_conditions)


# Output

<b>wp_scored_city_articles_by_state.csv </b> - Output File

The file is of the following schema which contains merged data from all the data sources:

Columns : <b> state </b>, <b> regional_division </b>, <b> population </b>, <b> article_title </b>, <b>revision_id </b>, <b>article_quality </b>

Analysis 1 : Top 10 US states by coverage: The 10 US states with the highest total articles per capita (in descending order) 

![image](./Output/Analysis_1.png)

Analysis 2 : Bottom 10 US states by coverage: The 10 US states with the lowest total articles per capita (in ascending order) 

![image](./Output/Analysis_2.png)

Analysis 3 : Top 10 US states by high quality: The 10 US states with the highest high quality articles per capita (in descending order)

![image](./Output/Analysis_3.png)

Analysis 4 : Bottom 10 US states by high quality: The 10 US states with the lowest high quality articles per capita (in ascending order)

![image](./Output/Analysis_4.png)

Analysis 5 : Census divisions by total coverage: A rank ordered list of US census divisions (in descending order) by total articles per capita

![image](./Output/Analysis_5.png)

Analysis 6 : Census divisions by high quality coverage: Rank ordered list of US census divisions (in descending order) by high quality articles per capita

![image](./Output/Analysis_6.png)

# License

This assignment code is released under the MIT License.

# Reflection and Addressing Questions


<b>1.) What biases did you expect to find in the data (before you started working with it), and why?</b>

I believed there would be a bias with the quality of articles with highest literacy rates such as New Hampshire, Alaska, Vermont etc having the best coverage of articles per capita.

<b>2.) Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?</b>

As an aspiring data scientist, I believe that there is a constant threat to racial equality and diversity with most modern day Recommender systems, Word Embeddings and Large Language Models. Using Word Embeddings as an example, it is important to address that the similarity of [embeddings](https://blog.acolyer.org/2020/12/08/bias-in-word-embeddings/) are not influenced by the training data scraped from the internet which includes polarized opinions.Algorithms have a finely tuned ability to recognize and learn from social patterns which were prevalent previously and they overgeneralize those patterns. This affects more than race—the lack of diversity with recommendations also includes gender, sexuality, and disability. I believe we need to make efforts to remove these biases. What the world needs is the harmony between being data-informed and social nuance.

<b>3.) How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?</b>

I think it is important to remove inherent bias due to variables that might be impact the coverage such as confounding variables. A researcher can add a factor of the literacy rate as a division factor with the article per capita ratio to address and remove this bias.

This assignment served as a great follow up to the reproducibility assignment as there were multiple sources which needed to be merged. It involved documenting the code well and checking shape and structure of dataframes to make it reproducible
