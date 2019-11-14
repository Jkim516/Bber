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
    
# EDA & Visualization

* Folium Map Visualization with markers representing bike stations. Lines from stations to stations representing total count of trips of that route. 
![folium_map_visualization1](https://user-images.githubusercontent.com/48810540/68901707-43098500-06eb-11ea-9e36-95b84f274efa.png)
* Heatmap of trip popularity (traffic) with trip count lines.
![folium_map_visualization2](https://user-images.githubusercontent.com/48810540/68901708-43098500-06eb-11ea-8767-a7431c3efdfd.png)

# Time Series Analysis
Weekdays on the bike share network are very different from weekends. This becomes very obvious when you plot the total number of trips, per hour and per day. In the elegant rainbow plot below, it is clear that (Monday to Friday) are incredibly similar. Trips starts to peak at 5:00 am until 9:00 am (most likely the morning commute) and another at 4:00 pm to 6:00 pm (most likely the evening commute). Lunchtime (11 to 1) also shows increased activity.  The weekend on the other hand is a completely different graph, there are no sharp peaks, simply a constant increase in activity until midday and then a constant decrease.
* <img width="640" alt="global_hourly_trend" src="https://user-images.githubusercontent.com/48810540/68901380-afd04f80-06ea-11ea-8ffa-082b0329ad2b.png">

The time-series graph shows each station must have its own temporal profile, a characteristic time-series that says something about how and when that station is used. If a station peaks early in the weekday morning and then never again, it could mean that this stations primary purpose is transporting people to work. Likewise if a station peaks at 6pm but never again then it could be considered an evening commute station. Other patterns might also exists that lend themselves to easy interpretation.

- Trips starts to peak during morning commute (between 5:00 and 9:00)
- Lunch time is also active (between 12.00 and 14.00)
- Trip again peaks at 6pm considering an evening commute.

## Modeling
Each bike stations hourly demand have trend and seasonality based on the time-series. Therefore, Facebook Prophet model can forecast time series data based on an additive model where non-linear trends. It is fast and provides completely automated forecasts. 

* [Prophet](link)

## Final 
- 

## Contact
I can be find in [Linkedin](www.linkedin.com/in/JungmoKim90) | [Github](https://github.com/Jkim516) for more details. 
