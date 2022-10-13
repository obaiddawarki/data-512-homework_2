# Human Centered Data Science - Homework_2

#About the Project - Considering Bias in Data
The repository contains the code and the data to reproduce the results and explore the concept of bias in data using Wikipedia articles. As a part of this project, we have considered articles on political figures from different countries. We combined a dataset of Wikipedia articles with a dataset of country populations , and use a machine learning service called ORES to estimate the quality of each article. Our analysis covers the politicians on Wikipedia and the quality of articles about the politicians varying among countries. The analysis consist of a series of tables that show:

1. The countries with the greatest and least coverage of politicians on Wikipedia compared to their population.
2. The countries with the highest and lowest proportion of high quality articles about politicians.
3. A ranking of geographic regions by articles-per-person and proportion of high quality articles.


The data analysis for this project includes data acquisition, data processing and analyzing the results.This homework was the part of Human Centered Data Science at the University of Washington - Seattle for Autumn 2022. The project contains all the details to reproduce this analysis independently on any machine without the use of any specific software package.

## API Documentation
The data that lists Wikipedia articles of politicians was crawled to generate a list of Wikipedia article pages about politicians from a wide range of countries using the API: [Category:Politicians by nationality](https://en.wikipedia.org/wiki/Category:Politicians_by_nationality). This data is available in the data folder with the file name as politicians_by_country.
To get the population dataset, we have used the [world population data sheet](https://www.prb.org/international/indicator/population/table)


## Directory Structure
The directory structure for the repository has been shown below in the form of a tree.

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

### Name of the file : population_by_country_2022_cleaned
The data file population_by_country_2022_cleaned csv has the following columns with their descriptions
continent	region	country	population

| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `continent`                    | Name of the continent to which the country belongs                            |
| `region`                   | Name of the region within the continent where the country lies                    |
| `country`                    | Name of the country                                                             |
| `population`               | Population of the country (in millions)                                           |

### Name of the file : politicians_by_country_SEPT_2022

The data file politicians_by_country_SEPT_2022 csv has the following columns with their descriptions
continent	region	country	population

| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `name `                    | Name of the politician                                                            |
| `url`                   | url for the article on wikipedia for the politician                   |
| `country`                    | Name of the country                                                             |

article_title	revision_Id	article_quality	country	region	population

### Name of the file : wp_politicians_by_country

| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `article_title`                    | Name of the article                          |
| `revision_Id`                   | Revision Id of an article               |
| `article_quality`               |Quality of an article                                      |
| `country`               | Name of the country                                           |
| `region`                   | Name of the region within the continent where the country lies                   |
| `population`                    |  Population of the country (in millions)                                           |

# Research Implications

## License

This code is available under the [MIT License](LICENSE)

Wikimedia [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en)
