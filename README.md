# Continentality
> Predicting average temperatures through regression for the state of Bahia

# About
Continentality is a measure of difference between continental and marine climates which is characterized by increased range between day time and night temperatures that occurs over land compared with water. That happens because of the
specific heat of the water is many times (approx. 5) smaller compared with land which thus makes the temperature rates around them slower to change.   

The task then was to analyze the effects of continentality at the extreme points of the state of Bahia.

## Challenge
In order to do so we were provided with data from 25 cities out of 417 (**approx 6% coverage**) from which the state of Bahia is consisted. As shown below, the dataset presents information on latitude, longitude, altitude and average 
temperatures for each month from the year of 1999 to 2019. 

Our goal then was to try to build a regression model to learn how to predict average temperatures for every city in the state of Bahia given its altitude, lat, long for a given period of time (month and year). 

<p align="">
  <img src="https://i.imgur.com/I0p6V4c.png">
</p>

> The figure below demonstrates the dataset coverage in terms of the cities in which data was available. We can see a plot of the average temperatures for the year of 2019.
<p align="">
  <img src="https://i.imgur.com/V1iEYtB.png">
</p>

# Models
As the goal was to train regression models to fit the data, we evaluated the Linear, Polynomial and Multivariate regression approaches. For the Linear and Polynomial regression approaches, the heuristics consisted of relating each of the variables with Temperature (e.g., Temperature x Altitude, Temperature x Latitude, Temperature vs Longitude and so on). Through this we obtained 5 curves (for each linear and non-linear model) that enable inferring the temperature value for each of the input variables. Therefore for each regression model we had 5 temperature predictions of which we used to compute the final prediction by taking the average between them. This is a terrible heuristic since it considers that the variables are independent. That was not the case for the multivariate regression model, as it goes through an optimization process that relates these variables by finding coefficient values for each of them.  


# Product

<p align="">
  <img src="https://i.imgur.com/y1KuW9c.png">
</p>

## Correlation - Relief

<p align="Center">
  <img src="https://github.com/FalsoMoralista/Continentality/blob/main/Plots/mapa-relevo-bahia.jpg?raw=true" height="560px">
</p>
