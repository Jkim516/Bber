# Bike N' Ride
The Bike N' Ride is a tool I developed to provide demand of bike stations in LA Downtown by predicting number of bikes availability in any given 1 hour time period. The Dataset is subset of [Metro Bikeshare Data](https://bikeshare.metro.net/about/data/). Bike N' Ride deployed onto web application using Heroku [Bike N' Ride](https://bike-n-ride.herokuapp.com/). The project can be found at the [Github](https://github.com/Jkim516/Bber).

#### -- Project Status: [Completed]

## Project Intro/Objective
The purpose of this project is forecasting demand of Metro Bikeshare in LA Downtown by predicting the number of bikes that will be available in any given 1 hour time-period.

### Methods Used
* Inferential Statistics
* Machine Learning - Random forest (Regression)
* Data Visualization - Matplot, Seaborn, FoliumMap 
* Predictive Modeling - Timeseries Analysis (Facebook Prophet)
* etc.

### Technologies
* Python
* Time-series (Prophet) / Regression (Random Forest), Scikit-Learn
* Matplot, Seaborn, Folium
* Request, Json, Pickle
* Heroku
* HTML
* Flask/JavaScript 
* etc. 

## Project Description
Urban bikeshare systems are a wonderful way to get around a city. Bikeshare is a great transit option for both commuter and tourist. However, it can be a frustrating experience to arrive at the bike station discover that there are no bikes available. The Bike N' Ride app provides not only live station status, but also number of bikes available next hour on each stations.

- Find most popular bike station 
- Find Monthly, Daily, and Hourly trend 
- Make a Prediction Model (Time-series / Regression)
- Predict the hourly demand (Trip-starting stations & Trip-ending stations) for each bike stations 

## Data Preparation
Three different Datasets are available from [Metro-Bikeshare](https://bikeshare.metro.net/about/data/). Every bikes trip Data from 2016 Q3 to 2019 Q3 (Updates the dataset every quarter). Next, Station Information Data with bike station address. Finally, Live Data with live status of how many bikes available and docks open for every bike stations.
1. Trip Data:
    - start_station & end_station
    - start_time & end_time
    - start_lat & start long
    - Bike_id
2. Station Info Data: 
    - station_ID
    - station_Name
    - region
3. Live Data: 
    - Number of BikesAvailable
    - Number of DocksOpen
    
## EDA & Visualization

# Time Series Analysis
* [Global hourly trends by day of week](https://github.com/Jkim516/Bber/Flask/images/global_hourly_trend.png)

## Modeling
Each bike stations hourly demand have trend and seasonality based on the time-series. Therefore, Facebook Prophet model can forecast time series data based on an additive model where non-linear trends. It is fast and provides completely automated forecasts. 

* [Prophet](link)

## Final 
- 

## Contact
I can be find in [Linkedin](www.linkedin.com/in/JungmoKim90) | [Github](https://github.com/Jkim516) for more details. 