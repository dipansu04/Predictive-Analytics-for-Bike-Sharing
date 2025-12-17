# Predictive-Analytics-for-Bike-Sharing
# Bike Sharing Demand Prediction
> A Multiple Linear Regression model to predict the demand for shared bikes based on meteorological and time-based variables.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
- **Project Background:** A US bike-sharing provider, BoomBikes, has suffered a considerable dip in revenues due to the ongoing Corona pandemic. The company aspires to understand the demand for shared bikes among the people once the lockdown is over to prepare themselves to cater to the people's needs effectively.
- **Business Problem:** The objective is to model the demand for shared bikes with the available independent variables. Management will use this model to understand how exactly the demands vary with different features and manipulate the business strategy accordingly.
- **Dataset:** The dataset contains daily bike rental counts along with weather information (temperature, humidity, windspeed) and categorical details (season, month, holiday, weekday).

## Technologies Used
- **Python** - version 3.x
- **Pandas** - for data manipulation
- **NumPy** - for numerical computations
- **Matplotlib** & **Seaborn** - for data visualization
- **Scikit-learn** - for data splitting, feature scaling (MinMaxScaler), and RFE
- **Statsmodels** - for building the Linear Regression model (OLS) and calculating VIF

## Conclusions
The final Multiple Linear Regression model achieved an **R-squared of approx. 81.6%** on the training data. The analysis identified the following key factors driving bike demand:

1.  **Temperature (`temp`):** The most significant variable (Coefficient: ~0.56). Demand increases substantially as temperature rises.
2.  **Year (`yr`):** A positive coefficient (~0.23) indicates a growing popularity of the service year-over-year (2019 had higher demand than 2018).
3.  **Weather Conditions:**
    * **Humidity (`hum`)** and **Windspeed (`windspeed`)** have negative coefficients, meaning high humidity and strong winds reduce demand.
    * **Bad Weather** (Mist/Cloudy) also negatively impacts rentals.
4.  **Seasonality:**
    * **Winter** and **Summer** seasons show higher demand compared to Spring.
    * **September** is a peak month for rentals.
