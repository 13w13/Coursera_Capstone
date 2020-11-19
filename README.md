# Clustering the Neighbourhoods of French cities : End of IBM DS Certificat Pro Project
---
Simon Weiss
~5 days development

Notebook link : https://13w13.github.io/IBM-Data-Science-Certificat-Pro/ 

## 1. Introduction

The Covid 19 crisis has been shaking the world now for more than 6 months. Faced with the health emergency, many governments, notably those of European countries, have for many made the choice of health over economic life by choosing to confine its population and close its borders. One of the consequences of these policies is to radically change the daily lives of citizens around the world, especially in cities.

## 2. Business Problem

The aim of this project is to identify what characterizes French cities in their decomposition in terms of neighborhood and venues.
Thanks to this decomposition, we will be able to understand in part the choices of economic specification in France.
This could help to identify the strengths, but also the weaknesses of the French economy when crises like the one we are experiencing with Covid hit the world. Are French cities highly dependent on the tourism sector? What about the commercial sector in this festive period that is coming up? We understand here that our conclusion in this project is aimed at interested citizens but also at the stakehodlers (city hall, government etc ... ) to better identify the sectors to be protected in their cities.

## 3. Data Description

### 3.1 Rank Cities in France

In order to perfom an analysis in the 5., we will reduce our clustering to the top 10 of french cities. 

To do that, we scrape our data from https://en.wikipedia.org/wiki/List_of_communes_in_France_with_over_20,000_inhabitants

This wikipedia page has information about list of big communes in France and provide us a ranking by inhabitants.

1. *Commune* : Name of Commune
2. *Department* : Name of Department
3. *Region* : Name of Region
4. *Population, 2013* : Population at year 2013
5. *Population, 2017* : Population at year 2017
6. *Rank* : Rank based on the Population at year 2017
In order to perfom an analysis in the 5., we will reduce our clustering to the top 10 of french cities. 


## 3.2 Get french cities and their neighbourhoods

We use JSON data available at https://www.data.gouv.fr/fr/datasets/r/34d4364c-22eb-4ac0-b179-7a1845ac033a

1. *codePostal* : Postal codes for France
2. *codeCommune* : Code for Commune in France
3. *nomCommune* : Name of the boroughs (for big cities), equivalent to Commune in France
4. *libelleAcheminement* : Name of city

## 3.3 Foursquare API Data

To meet the need identified above, we are going to need the different venues of cities in France. 
Thanks to the Foursquare API, we will find this information. The API needs GPS codes (geocoding) to work. 

The api gives the following information : 

1. *Neighbourhood* : Name of the Neighbourhood
2. *Neighbourhood Latitude* : Latitude of the Neighbourhood
3. *Neighbourhood Longitude* : Longitude of the Neighbourhood
4. *Venue* : Name of the Venue
5. *Venue Latitude* : Latitude of Venue
6. *Venue Longitude* : Longitude of Venue
7. *Venue Category* : Category of Venue


## 4. Methodology

We are going to collect the maximum amount of data on cities in France in a first step in order to perform our clustering on the largest number of cities.   
This clustering would be done according to the different venues categories that the foursquare API will provide us.
This provides a complete, ready-to-use clustering for further analysis. We could think of a report for the French government for example.   
For this project here, we will filter our results to the Top 10 cities in France and present our conclusions. 

In the meantime, we are going to build different maps of cities in France and then of the different clusters. 

Good reading ! 
