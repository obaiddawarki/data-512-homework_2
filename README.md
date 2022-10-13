# Human Centered Data Science - Homework_2

# About the Project - Considering Bias in Data
The repository contains the code and the data to reproduce the results and explore the concept of bias in data using Wikipedia articles. As a part of this project, we have considered articles on political figures from different countries. We combined a dataset of Wikipedia articles with a dataset of country populations , and use a machine learning service called ORES to estimate the quality of each article. Our analysis covers the politicians on Wikipedia and the quality of articles about the politicians varying among countries. The analysis consist of a series of tables that show:

1. The countries with the greatest and least coverage of politicians on Wikipedia compared to their population.
2. The countries with the highest and lowest proportion of high quality articles about politicians.
3. A ranking of geographic regions by articles-per-person and proportion of high quality articles.


The data analysis for this project includes data acquisition, data processing and analyzing the results.This homework was the part of Human Centered Data Science at the University of Washington - Seattle for Autumn 2022. The project contains all the details to reproduce this analysis independently on any machine without the use of any specific software package.

## Data Set Source
The data that lists Wikipedia articles of politicians was crawled to generate a list of Wikipedia article pages about politicians from a wide range of countries using the API: [Category:Politicians by nationality](https://en.wikipedia.org/wiki/Category:Politicians_by_nationality). This data is available in the data folder with the file name as politicians_by_country.
To get the population dataset, we have used the [world population data sheet](https://www.prb.org/international/indicator/population/table)

## Relevant API
The relevant APIs for this repository have been mnentioned below:
1. [ORES](https://www.mediawiki.org/wiki/ORES)
2. [Wikimedia Foundation REST API terms of use](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)


## Directory Structure
The directory structure for the repository has been shown below in the form of a tree:

```

.
├── data
│   ├── Cleaned_data
│       ├── population_by_country_2022_cleaned.csv
│   ├── csv_files
│       ├── politicians_by_country_SEPT_2022.csv
│       ├── population_by_country_2022.csv
│   ├── output
│       ├── article_quality.json
│       ├── article_revisions_test.json
│       ├── wp_countries-no_match.txt
│       ├── wp_politicians_by_country.csv
├── src
│   └── hcds-a2-considering-bais-in-data.ipynb
├── README.md
└── LICENSE
```

### Data Description
The data description of the files included in this repository with the column description is shown as below:

### Name of the file : population_by_country_2022_cleaned.csv
The schema consists of countries, region and population for each country/region. The data file population_by_country_2022_cleaned csv has the following columns with their descriptions

| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `continent`                    | Name of the continent to which the country belongs                            |
| `region`                   | Name of the region within the continent where the country lies                    |
| `country`                    | Name of the country                                                             |
| `population`               | Population of the country (in millions)                                           |

### Name of the file : politicians_by_country_SEPT_2022.csv
Consists of crawled Wikipedia article pages about politicians different countries. The data file politicians_by_country_SEPT_2022 csv has the following columns with their descriptions

| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `name `                    | Name of the politician                                                            |
| `url`                   | url for the article on wikipedia for the politician                   |
| `country`                    | Name of the country                                                             |


### Name of the file : wp_politicians_by_country.csv
This file consists of data output with politicians mapped to countries and region, basically the data table used for analysis. The data file wp_politicians_by_country.csv has the following columns with their descriptions


| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `article_title`                    | Name of the article                          |
| `revision_Id`                   | Revision Id of an article               |
| `article_quality`               |Quality of an article                                      |
| `country`               | Name of the country                                           |
| `region`                   | Name of the region within the continent where the country lies                   |
| `population`                    |  Population of the country (in millions)   

# Input Data:
The input data for the analysis include the 2 csv files that are present in the data folder with the names 
- population data (population_by_country_2022_cleaned.csv)
- Politicians data (politicians_by_country.SEPT.2022.csv) 

# Output Data:
The output folder consists of the files that are generated as a part of this analyis(csv and txt files) and some are part of the intermediate state (JSON files)

The files that are the part of the output are mentioned below:
- wp_countries-no_match.txt (All countries for which population dataset does not have an entry for the equivalent Wikipedia country, or vice-versa)
- wp_politicians_by_country.csv (Refined data output with politicians mapped to countries and region, basically the data table used for analysis)

The files that are intermediate and are genearted in between as the part of the analysis are stored in the output folder are mentioned below:
- article_quality.json (JSON file containing the article quality for the respective articles)
- article_revisions_test.json (JSON file containing the article revision id for the respective articles)


# Research Implications:
One of the lessons that I learned from the dataset is that it is very important to have a domain knowledge when we analyze a given dataset.There is a big difference with the numner of wilikpedia articles of politicans per million population on the regional level. The data that was collected is from the English Wikipedia that constitutes of the english articles and hence there is a potential bias towards the english speaking regions. This could be one of the reasons for the big differences at the regional level.

Q1: What (potential) sources of bias did you discover in the course of your data processing and analysis?
One of the bias is the language spoken in the country. If we have more English speakers in the country, there is a maximum likelihood for the more articles for that country. Another potentail bias that could be seen is that the countries where the access for internet is good contribute more to the wikipedia and hence as such result in more articles.

Q2: What might your results suggest about (English) Wikipedia as a data source?
The results suggest that there is more data on Wikipedia for the English speaking politicans and as such the policymakers, researchers shoukd keep this in mind before imolemnting any policy as the data that leads to make the conclusion about any region would be biased towards the one section of the politicans (English speakers).

Q3: Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
A realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data, is if the data is used to study a phenomenon that is not well represented by the data. For example, if the data is used to study the effect of a new medication on a disease, but the data only includes a small number of patients with the disease, the results may be biased or misleading. Similar is the case in our dataset where the data was biased towards the English speaking politicans. Thus due to the inherent gaps and limitations of the data, using these data to train a model, perform a hypothesis-driven research, or make business decisions might create biased or misleading results.

 
## License

This code is available under the [MIT License](LICENSE)

Wikimedia [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en)
