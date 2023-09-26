# Continentality
> Predicting average temperatures through regression for the state of Bahia

# About
Continentality is a measure of difference between continental and marine climates which is characterized by increased range between day and night-time temperatures that occurs over land compared to water. That happens because of the specific heat of the water is many times (approx. 5) smaller compared to land which thus makes the temperature rates of the regions around them slower to change.

## Challenge
In this regard we were asked to analyze the effects of continentality at the extremities of the state through curve fitting models.

In order to do so we were provided with data from 25 cities (out of 417) - **an approximate 6% coverage** - from which the state of Bahia is consisted. As shown below, the dataset presents information on latitude, longitude, altitude and average temperatures from a few metereological stations for each month between the years of 1999 to 2019. Therefore we tried to build a regression model that allowed to predict average temperatures for every city in the state (for which we lacked data) given its altitude, lat, long and given a period of time (month and year). 

<p align="">
  <img src="https://i.imgur.com/I0p6V4c.png">
</p>

###  It is quite straightforward to see that to learn the task accurately means, in someway, to check the hypothesis that average temperatures can be inferred from lat, long and altitude, but another aspect that we wanted to verify was whether prediction precision correlated with the distance to the nearest climate station for the cities in which the data was absent. 

> The figure below demonstrates the dataset coverage in terms of cities in which data was available. We can see a plot of the average temperatures for the year of 2019.
<p align="">
  <img src="https://i.imgur.com/V1iEYtB.png">
</p>

# Practice
The first step was to train the models to fit the data so we choosed to evaluate the Linear, Polynomial and Multivariate regression approaches. Considering that for the Linear and Polynomial regression approaches we could only relate the dependent variable (temparature) to one of the independent variables, the heuristics consisted of fitting one curve for each of the independent variable (e.g., Temperature x Altitude, Temperature x Latitude, Temperature vs Longitude and so on). 

Through this, for each regression model we had 5 temperature predictions of which we used to compute the final prediction by taking the average amongst them. This is a terrible heuristic since it considers that these variables are independent. That was not the case for the multivariate regression model, as it goes through an optimization process that relates these variables by finding coefficient values for each of them (fitting a hyperplane to the data).  

Complementary data
[...]

Analysis/Results
[...] the effects of continentality are most significantly observed at the variance over daily-level average temperatures [...]
# Product

<p align="">
  <img src="https://i.imgur.com/y1KuW9c.png">
</p>

## Relief Map
<p align="Center">
  <img src="https://github.com/FalsoMoralista/Continentality/blob/main/Plots/mapa-relevo-bahia.jpg?raw=true" height="560px">
</p>

