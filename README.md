# Impact of Crime on Housing Prices in Chicago

### Motivation
Safety has been considered a fundamental human right since the beginning of the beginning of the human rights era. Maintaining Law and Order is one the most basic and important responsibilities of any local government. Crime rate thus becomes a very important indicator for comparing neighborhoods. One of the most studied effects of crime is the impact it has on the housing and rental rates in any communities. One of the easiest ways to measure crime is to explore the housing and rental rates in a given area. The goal of this project is to study the relationship betweeen crime rate and housing prices in Chicago city and the to discover patterns in the types of crimes that effect housing prices more than others.

### Previous Work
My inspiration for this analysis is based on the work done by Harold Li that can be found on [Databucket](https://databuckets.org/databucket/2016/01/exploring-chicago-crime-and-housing.html). The analysis for this research was based on Trulia API data. The results from his work showed that crime rates inversely impact housing rates and there is a non-linear relationship between them. To add to this analysis, I would like to also see if different crime types have different effects on the housing prices.
     
### Research Questions

 - **H1.0:** Is there a strong relationship between crime rates and housing prices in Chicago at the neighborhood level? Are changes in  crime rates a strong predictor for changes in housing prices?  
     
  
  
 - **H2.0:** Do different types of crimes have different effects on the housing prices?  
     
### Methodology
- For determining the relationship between the crime rates and the housing prices (H1.0), I will perform a linear regression (housing price ~ crime rate) to understand the relationship between the crime rates and housing prices. This would involve trying different models (ridge, lasso,, etc.) and finding any non-linear relationships (log-linear, etc.).  
The ![equation](https://latex.codecogs.com/gif.latex?R%5E2) value will determine whether changes in crime rates are a strong predictor for housing prices.
- For determining the effect of different types of crimes on the housing prices (H2.0), I plan to fit a linear regression (housing price ~ crime rate + crime type) to see whether there is a substantial difference between the coefficients of different crime types. I also plan to perform an Anova test to determine whether the crime type has a significant effect on the housing prices.

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
│   └── housing_price_distributions.png
├── LICENSE
├── README.md
├── data-preparation.ipynb
└── final-project-report.ipynb  

```

### Dataset
For this project I have used four different datasets to create data for my analysis. I used the [Zillow Dataset](https://www.zillow.com/research/data/) to get the housing prices for neighborhoods in Chicago. For crime I used the Chicago Crimes dataset that is publically available on [the official website of the City of Chicago](https://data.cityofchicago.org/Public-Safety/Crimes-2019/w98m-zvie). In order to normalize the crime counts based on the neighborhood poplulations, I used the 2010 Census data for the population at neighborhood level. The data is available from the [Datahub website](https://datahub.cmap.illinois.gov/dataset/community-data-snapshots-raw-data/resource/8c4e096e-c90c-4bef-9cf1-9028d094296e?inner_span=True). Finally for mapping the latitude-longitude coordinates in the crime dataset to Zillow defined neighborhoods, I used the nieghborhood boundary data generated in the [github repository](https://github.com/mashvisor/us-neighborhoods-boundaries/blob/master/out/csv/IL-Regions.csv).  

### Licence
This code is available under the [MIT License](LICENSE)  

Zillow's dataset is available under the following [Terms of Use](https://www.zillow.com/z/corp/terms/)  

All data from the Chicago Open Data website is available for use under the following [Data Terms of Use](https://www.chicago.gov/city/en/narr/foia/data_disclaimer.html)  
