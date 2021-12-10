---
layout: default
---

Hi and welcome to my Data Science project on Biking trends in NYC. 

![Citi Bike Station](citistation.jpg)

# Project Intro

I started this project to see how biking/cycling has evolved in NYC. I wanted to see how biking grew in popularity throughout NYC and also how dangerous it has grown or decreased.Thanks to Citi Bike I was able to determine where biking was more popular and through data from OpenDataNYC I was able to determine which areas were more dangerous

## Overview

I hypothesize that the borough that bikes the most is Manhattan especially in 2014 and in 2021 but in 2021 people in other boroughs will start to grow more interested in biking. I also hypothesize that the most dangerous borough for biking will be Manhattan both in 2014 and 2021 since its where biking is probably most popular. CitiBike's travel data allowed me to have a reasonable estimation of where biking is most popular by checking which of its bike stations are most popular. I used OpenDataNYC collision data to see where the most collisions occurred. Some methods I used were cleaning up data(like grouping, dropping certain data, summing duplicates), merging multiple csv files, mapping data points on folium, making bar graphs with matplotlib.pyplot. Some of the tools I used were Folium, Numpy, Matplotlib.pyplot, Pandas, and pandas.pydata.org.

### Data

**CitiBike Travel Data:** I used this data set to determine the most popular bike stations and thus coming up with an estimation of which boroughs bike the most. The data sets were grouped by month having trip data by bike. Most important columns for this project were the latitude and longitude of the starting bike station and the name of the bike station.

**OpenData Collisions Data:** This data set was used to determine most dangerous boroughs for biking. This data set had collision data dating from 2012 to 2021 and had unique collision ids for each collision as well as where the collision took place.

### Techniques

The CitiBike travel data was a huge help having the longitude and latitude of each bike station but it I didnt need separate travel information so I had to clean up the data by adding how many times each bike station showed up in the file. Since the Citibike travel data came per month and I wanted popular bike stations per year I had to merge the data after getting the times each bike station was visited I did this for the year 2014 and 2021. After that I used folium to place markers on a map which correspond to the 100 most popular bike stations for each year. For the OpenData Collision data I had to remove any rows that had missing information. I decided to remove rows with any thing missing just incase they could be duplicates but it didn't look like a duplicate because of missing data. I then grouped the data by borough and summed up the amount of injured cyclists per borough. I used matplotlib.pyplot to graph this data.

### Popular Bike Stations 2014:

<iframe src="2014Map.html" height="500" width="500"></iframe>

Here you can see the 100 most popular bike stations in 2014. My hypothesis was correct and Manhattan is the most popular borough for biking. We can even determine that lower Manhattan has more cyclists than upper Manhattan.

### Popular Bike Stations 2021:

<iframe src="2021map.html" height="500" width="500"></iframe>

Here you can see the 100 most popular bike stations in 2021. Here my hypothesis was only half correct, Manhattan is still the most popular borough for biking but biking has not spread out into the other boroughs as much as I hypothesized. Upper Manhattan does start to see more bike activity in 2021 than 2014.

### Most Dangerous Boroughs for Biking:

![Collisions by Borough for 2014 and 2021](collisionsbargraph.png)

Here you can see that the most dangerous borough for biking is Brooklyn followed by Manhattan for both 2014 and 2021 but you can see that overall injuries to cyclists has decreased since 2014 particularly for Manhattan and Brooklyn.

#### Citations

[CitiBike Travel Data](https://ride.citibikenyc.com/system-data)

[OpenData Collisions Data](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)

[Citi Bike Image](https://ny.curbed.com/2020/4/14/21220752/citi-bike-coronavirus-healthcare-workers-commute)


