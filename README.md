# Geospatial-data-project.-New-office-location
Third Ironhack project

![AMS image](https://d1csarkz8obe9u.cloudfront.net/posterpreviews/amsterdam-postcard-design-template-4e4e85c37c8e5a0b1258d3df0d98bf01_screen.jpg?ts=1581962219)

### Welcome to my third Ironhack project! The purpose of this project was mainly to decide the most appropriate location for a new startup office based on the following criteria team structure:

- 20 Designers
- 5 UI/UX Engineers
- 10 Frontend Developers
- 15 Data Engineers
- 5 Backend Developers
- 20 Account Managers
- 1 Maintenance guy that loves basketball
- 10 Executives
- 1 CEO/President

and the following desirable requirements for the location:

- Designers like to go to design talks and share knowledge. There must be some nearby companies that also do design.
- 30% of the company staff have at least 1 child.
- Developers like to be near successful tech startups that have raised at least 1 Million dollars.
- Executives like Starbucks A LOT. Ensure there's a starbucks not too far.
- Account managers need to travel a lot.
- Everyone in the company is between 25 and 40, give them some place to go party.
- The CEO is vegan.
- If you want to make the maintenance guy happy, a basketball stadium must be around 10 Km.
- The office dog—"Dobby" needs a hairdresser every month. Ensure there's one not too far away.

## Scope of the project
Given that it was impossible to prioritize all of the above requirements I selected 5 main ones to be considered, and the weight that each of them will have in the final evaluation:

- 1: Nearby startups (within 1km). For designers to speak with other designers in different startups (weight: 75%)
- 2: Schools in the area (within 1km). For the employee's kids (weight: 100%)
- 3: Nearby Starbucks (within 1km). For the executives (weight: 50%)
- 4: Airports and train stations (Airport within 10km or Amsterdam Central Train Station within 2km). For the account managers travelling (weight: 100%)
- 5: Bars (within 750m). Because it's important to have a good time after work ;) (weight: 50%)

I decided that the city I was going to search for the best locations was Amsterdam given that is currently considered as one of the main tech hubs in Europe.

## Approach and result
In order to perform the project I started off with a database that I had previously worked with in Mongo called "companies", which sotred several information of over 25k companies around the world, including office location with latitude and longitude values. From that starting point I executed some queries to filter only those companies that were based in Amsterdam in order to use it as my potential range of office locations for this new startup. 

In terms of analysing the nearby requirements I used solely the Foursquare API to make calls in order to get the specific locations of places such as schools, bars, airports, and other startups. Once I had that data I created new collections in Mongo in order to use them to make geoqueries against them comparing those locations with the ones I had already extracted from the companies database to analyse proximity.

The final result were the following top 3 locations (#1 is blue, #2 is red, #3 is black):

[![Ams-map.png](https://i.postimg.cc/Px8wnDsr/Ams-map.png)](https://postimg.cc/qh4R8zv9)

## Sources and libraries used
- Pandas - https://pandas.pydata.org/
- Pymongo - https://pymongo.readthedocs.io/en/stable/
- Folium - http://python-visualization.github.io/folium/
- JSON - https://docs.python.org/3/library/json.html
- Requests - https://docs.python-requests.org/en/master/
- Foursquare(for API calls) - https://developer.foursquare.com/

## Files structure
Simple structure ;):
- "Jsons" folder containing the all the json folders created which I then imported to Mongo in order to make geoqueries.
-  "Office location analysis-Amsterdam" jupyter notebook containing all the analysis perfromed with orientative and detailed comments.
# That's all! Thank you for your interest :)