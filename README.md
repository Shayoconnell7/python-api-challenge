# python-api-challenge

## Part I - WeatherPy

I started by importing dependencies and my API Key. I also set the range of latitudes and longitudes for citipy to pull from.

I set params, and used the API to call information about each city provided by citipy. I stored the wind speed, humidity, cloudiness, and maximum temperature of each city along with the coordinates and country in a new dataframe, and exported it as a csv file. 

I also removed any cities where the humidity was greater than 100% using a .loc.

I then created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

I further separated the cities into Northern and Southern Hemisphere, then ran a linear regression on each relationship. I had to set all of the variable to integers using .astype in order to accomplish this.

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude





### Part II - VacationPy


* I began by importing my dependencies and the csv file I created in part I.
* I then created a heat map that displayed the humidity for each city.

* When I used my actual ideal conditions to narrow down the results, it returned far too many, so I had to narrow them significantly in order to reach a "reasonable number". 

* Using Google Places API I found the first hotel for each city located within 5000 meters of my ideal city coordinates.

* Finally I plotted hotels on top of a humidity heatmap with each pin containing the Hotel Name, City, and Country.


# My analysis/final considerations:
    1. Although there is a high correlation between Latitude and Max Temperature, there was almost no correlation between Latitude and any of the other measures. I surmise that there must be more factors at play - for example, distance from the ocean might affect humidity, elevation and landscape features might affect wind speed, etc.
    
    2. There may be more correlation between Latitude and other measures we did not collect, such as precipitation. It would be interesting to explore more weather-related measures as well.
    
    3. This data is only for a single day - it would probably be much more useful to look at weather trends over time in relation to Latitude, as we have no idea how representative the day I collected that data is for the general weather patterns in the areas.
   
    4. There are far more important criteria when choosing a vacation spot than we have here. I think it would be good (in a real-world scenario) to compare more measures (like terrain, cleanliness, cost, etc) with a wider range of 'ideal weather conditions' before narrowing it to such a short list. 


(heatmap_with_markers.png)

