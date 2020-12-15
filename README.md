# Impact of Crime on Housing Prices in Chicago

## Data Source
For this project I have used four different datasets to create data for my analysis. I used the [Zillow Dataset](https://www.zillow.com/research/data/) to get the housing prices for neighborhoods in Chicago. For crime I used the Chicago Crimes dataset that is publically available on [the official website of the City of Chicago](https://data.cityofchicago.org/Public-Safety/Crimes-2019/w98m-zvie) under the following [Terms of Use](https://www.chicago.gov/city/en/narr/foia/data_disclaimer.html). In order to normalize the crime counts based on the neighborhood poplulations, I used the 2010 Census data for the population at neighborhood level. The data is available from the [Datahub website](https://datahub.cmap.illinois.gov/dataset/community-data-snapshots-raw-data/resource/8c4e096e-c90c-4bef-9cf1-9028d094296e?inner_span=True). Finally for mapping the latitude-longitude coordinates in the crime dataset to Zillow defined neighborhoods, I used the nieghborhood boundary data generated in the [github repository](https://github.com/mashvisor/us-neighborhoods-boundaries/blob/master/out/csv/IL-Regions.csv). 

**Ethical Considerations:** Note that the Zillow dataset reports the Zillow Home Value Index (ZHVI) for All Homes (SFR, Condo/Co-op) based on Neighborhood. The ZHVI is derived as the median house price for all estimated house prices in an area and adjusted for seasonality and estimation errors. (More information about ZHVI can be read from [ZHVI Overview](https://www.zillow.com/research/zhvi-methodology-2019-highlights-26221/) and [a deep-dive into it's methodology](https://www.zillow.com/research/zhvi-methodology-2019-deep-26226/)) The dataset thus does not contain the actual housing price for any individual property. It also does not contain any additional information about home owners or buyers. The crime data does not contain any identifiers such as name, age, gender, race or religion of neither the criminals nor the victims. Both datasets do not leak any private information about any persons.

## Directory Structure

```
.
├── data
│   └── input
│        ├── Chicago_Crimes_Dataset_2019.csv
│        ├── chicago_population_data.csv
│        ├── IL-Regions.csv
│        └── zillow_zhvi_neighborhood_dataset.csv
│   └── out
│        ├── crime_data_with_hoods.csv
│        ├── crime_final.csv
│        ├── final_data.csv
│        └── housing_zhvi_final
├── images
│   ├── crime_vs_prices_regression.png
│   ├── crime_vs_prices_regression_log_scaled.png
│   ├── crimes_type_vs_prices_log_scale.png
│   ├── domestic_crime_vs_prices_regression_log_scaled
│   └── housing_price_distributions.png
├── LICENSE
├── README.md
├── data-preparation.ipynb
└── final-project-report.ipynb  

```

## Analysis Questions


## Licence
This code is available under the [MIT License](LICENSE)  

Zillow's dataset is available under the following [Terms of Use](https://www.zillow.com/z/corp/terms/)  

All data from the Chicago Open Data website is available for use under the following [Data Terms of Use](https://www.chicago.gov/city/en/narr/foia/data_disclaimer.html)  
