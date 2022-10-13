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
The data file population_by_country_2022_cleaned csv has the following columns with their descriptions
- continent	
- region	
- country	
- population

| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `continent`                    | Name of the continent to which the country belongs                            |
| `region`                   | Name of the region within the continent where the country lies                    |
| `country`                    | Name of the country                                                             |
| `population`               | Population of the country (in millions)                                           |

### Name of the file : politicians_by_country_SEPT_2022.csv
The data file politicians_by_country_SEPT_2022 csv has the following columns with their descriptions
- name 
- url 
- country

| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `name `                    | Name of the politician                                                            |
| `url`                   | url for the article on wikipedia for the politician                   |
| `country`                    | Name of the country                                                             |


### Name of the file : wp_politicians_by_country.csv
The data file politicians_by_country_SEPT_2022 csv has the following columns with their descriptions
- article_title 
- revision_Id 
- article_quality 
- country 
- region 
- population

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
The output folder consists of the files that are generated as a part of this analyis(csv and txt files) and some are part of the intermediate state (JSON files). 
The files that are the part of the output are mentioned below:
- wp_countries-no_match.txt
- wp_politicians_by_country.csv

The files that are intermediate and are stored in the output folder are mentioned below:
- article_quality.json
- article_revisions_test.json


# Research Implications

The three questions that I have answered include the following:

1. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?

If you were to use this data to train a model to generate new data, the results would be biased and misleading. This is because the data is limited and does not include all possible values. For example, the data does not include any values for people who are not employed. This would create a biased model that would only generate data for people who are employed. Similarly If a company was considering using this data to make business decisions, they might come to inaccurate conclusions about customer behavior. For instance, they might think that customers only shop on weekdays, when in reality there are simply fewer data points for weekends. This could lead to the company making poor decisions about staffing, advertising, and promotions. Additionally, the data does not include information about why customers are returning items, so the company would not be able to make informed decisions about how to improve its products or services.
 
 2. Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
 
Yes, I can think of a realistic data science research situation where using these data might still be appropriate and useful, despite its inherent limitations and biases. For example, if we were researching a new product or service and wanted to determine whether it was more popular with men or women, we could use these data to train a model that would predict the gender of new users. However, we would need to be aware of the limitations of the data and account for them in our analysis. It is possible that despite the inherent limitations and biases of this data, it could still be used for training a model, performing hypothesis-driven research, or making business decisions. However, it is important to note that the results of any analysis using this data may be limited in accuracy and may not be representative of the true population.
 
 3. 
 
## License

This code is available under the [MIT License](LICENSE)

Wikimedia [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en)
