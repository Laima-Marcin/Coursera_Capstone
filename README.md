# Coursera_Capstone
The Battle of Neighborhoods 

## Finding the best place for opening an Italian restaurant in London

**PART 1 - A description of the problem and a discussion of the background**

1.1 Target audience
This project is intended to help people who are planning to open an Italian restaurant in London how to choose the
right location by providing data about each borough of London and finding out the top venues for each borough and
checking if there are many other Italian restaurants already present in that area.
* The goal is to find the place with least competitors and highest population.

1.2 Discussion of the Background
 London is the capital and largest city of England and the United Kingdom.
 London's 2020 population is now estimated at 9,304,016 and it keeps growing.
 London is one of the most multicultural cities on the planet.
 One of the world’s most visited cities, London has something for everyone: from history and culture to
fine food. With such diversity, London’s cultural dynamism makes it among the world’s most international
cities.
 London is a city where businesses thrive.
 The Italian cuisine is at the top list of the Londoners’ diet.
 (M. Sannino, E. Robustelli, A. Biccario) – It is widely claimed that Londoners are obsessed with the Italian
food, or at least, the majority of them.
 Such popularity of the ‘Made in Italy’ is due to the quality of their products but also due to the intense
promotion made over the last few years.

1.3 Description of the Problem
Finding the best place to open an Italian restaurant in London requires some careful consideration, research and
preparation. Since there are over 39,338 food service establishments in London (restaurants, coffee shops, food
halls) we need deeper insight from available data in order to be able to make a decision where to establish the first
Italian restaurant.

**PART 2 - Data Acquisition and Processing¶**

In this project, I will be using the following datasets to help solve my problem 
 List of London Boroughs (from Wikipedia page), and Foursquare API.
Information on boroughs and their population & coordinates
 Population can be used to determine how big and how dense the specific borough is.
 Coordinates can be used to get neighborhood data from Foursquare and finding the most popular venues
in each borough and then clustering them by using K-means and analysing each cluster and finding which
cluster has least restaurants and least Italians restaurants and I will provide my observation which clusters
are most suitable and I will create a map using Folium library to show these clusters on London map.

2.1 - Data Source
Wikipedia url: https://en.wikipedia.org/wiki/List_of_London_boroughs
Foursquare API
 List of top 50 popular places in the neighborhood
 source: Foursquare
 url: https://api.foursquare.com

2.2 - Data processing
 Create a dataframe consisting of the columns BoroughName = [] Population = [] Coordinates = [] by using
BS4, BeautifulSoup

 Clean and analyse the data and find how many unique boroughs there are in London and what are their
coordinates (latitude and longitude)
 Create London map and show all the boroughs on the map from geopy.geocoders import Nominatim
 Create a function to explore all boroughs
 Get top 50 venues in 500m radius of the centre of each Borough
 Use One hot encoding before clustering
 Find top 10 venues for each neighbourhood and create pandas dataframe.
 Conduct K-means clustering to group the boroughs according to what convenience facilities they have
using Foursquare data.
 Add clustering labels
 Merge london_grouped with london_data to add latitude/longitude for each neighbourhood
 Create a map showing all the clusters.
 Analyse each cluster individually and find 3 most suitable clusters for opening an Italian restaurant and I
will create a map showing these 3 clusters.

