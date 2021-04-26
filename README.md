# python-api-challenge
Unit 6: APIs

### **<u>Part I - WeatherPy</u>**

Objective: Create a Python script to create a representative weather model of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy) and the [OpenWeatherMap API](https://openweathermap.org/api) to perform a weather check on 500+ random cities using a series of successive API calls (*Note: OpenWeatherMap API key required).

A series of scatter plots will showcase the following relationships (images can be found in WeatherPy folder):

* Temperature (F) vs. Latitude

  ![](C:\Users\pauls\Desktop\python-api-challenge\WeatherPy\Lat_Temp.png)

* Humidity (%) vs. Latitude

  ![](C:\Users\pauls\Desktop\python-api-challenge\WeatherPy\Lat_Humidity.png)

* Cloudiness (%) vs. Latitude

  ![](C:\Users\pauls\Desktop\python-api-challenge\WeatherPy\Lat_Cloudiness.png)

* Wind Speed (mph) vs. Latitude

  ![](C:\Users\pauls\Desktop\python-api-challenge\WeatherPy\Lat_Wind.png)

Next, run linear regression on each relationship after grouping cities into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

**WeatherPy Analysis:**

1. Scatter plot shows indicates city's latitude is related to its max temperature; max temp rises the closer a city's latitude nears to the equator (0).
2. Scatter plots for all other variables (humidity, cloudiness, wind speed) shows there's no relationship in regards to a city's latitude.
3. Linear regression graphs confirms the above assessment based on the r-value. In regards to the city's latitude vs. max temp, there is a strong correlation for cities in the Northern Hemisphere and a moderate correlation for cities in the Southern Hemisphere. There is no correlation between a city's latitude and it's humidity, cloudiness, or windspeed based on the r-values.

### <u>**Part II - VacationPy**</u>

Objective: Utilize weather data from Part I WeatherPy to plan a future vacation through the use of jupyter-gmaps and the Google Places API (*Note: Google API Key required).

* Heat map that displays humidity from every city from Part I (weather_data.csv located in WeatherPy/output_data folder)

  ![](C:\Users\pauls\Desktop\python-api-challenge\VacationPy\heat_map.PNG)

* Narrowed location search based on high humidity and high temperature

* Google Places API to find first hotel for each city located within 5000 meters of coordinates

  ![](C:\Users\pauls\Desktop\python-api-challenge\VacationPy\hotels.PNG)