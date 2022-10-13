# Human Centered Data Science - Homework_1

#About the Project
The repository contains the code and the data to reproduce the results for the analysis of the monthly views on the
dinosaurs articles on the English wikipedia ranging from July 2015 through September 2022. The data analysis for this project includes data acquisition, data processing and generating the time series analysis for the number of views for each dinosaurs articles. This homework was the part of Human Centered Data Science at the University of Washington - Seattle for Autumn 2022. The project contains all the details to reproduce this analysis independently on any machine without the use of any specific software package.

## API Documentation
The data acquisition was done from the Page View API and this API gives us the data at monthly granularity. The link for the API used in the analysis for this assignment : [Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews#Monthly_counts)

## Directory Structure
The directory structure for the repository has been shown below in the form of a tree.

```

.
├── raw_files
│   ├── dino_monthly_desktop_start201501-end202210.json
│   ├── dino_monthly_mobile-app_start201501-end202210.json
│   ├── dino_monthly_mobile-web_start201501-end202210.json
│   ├── dinosaur_genera_cleaned_SEPT_2022.xlsx
├── json
│   ├── dino_monthly_cumulative_start201501-end202209.json
│   ├── dino_monthly_desktop_start201501-end202209.json
│   └── dino_monthly_mobile_start201501-end202209.json
├── plots
│   ├── Max_Average_and_Min_Average_Page_Requests_for_Desktop_and_Mobile.png
│   ├── Top_10_Articles_by_Peak_Page_Views_and_Access_Type.png
│   └── Bottom_10_Articles_with_Fewest_Months_of_Data_for_Desktop_and_Mobile_Each.png
├── src
│   └── hhcds-a1-data-curation
├── README.md
└── LICENSE
```

## Data Description

| Column                    | Description                                                                        |
| ------------------------- | -----------------------------------------------------------------------------------|
| `year`                    | The year of the data point                                                         |
| `month`                   | The month of the data point.                                                       |
| `date`                    | The year-month pair serve as a key                                                 |
| `log_views`               | The natural log of the views column                                                |
| `access`                  | Data contains three different access: desktop, mobile-app, mobile-web              |
| `article`                 | This is the name of the articles we are pulling on Wikipedia                       |


## Visualization


![Maximum Average and Minimum Average](plots/Max_Average_and_Min_Average_Page_Requests_for_Desktop_and_Mobile.png)

![Top 10 Peak Page Views](plots/Top_10_Articles_by_Peak_Page_Views_and_Access_Type.png)

![Bottom Top 10 With Fewest Months](https://github.com/obaiddawarki/data-512-homework_1/blob/main/plots/Bottom_10_Articles_with_Fewest_Months_of_Data_for_Desktop_and_Mobile_Each.png)

## License

This code is available under the [MIT License](LICENSE)

Wikimedia [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en)
