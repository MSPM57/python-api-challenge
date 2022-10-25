# python-api-challenge
api calls


 in WeatherPY jupiter notebook:
# Incorporated citipy to determine city based on latitude and longitude
from citipy import citipy

# Output File (CSV)
output_data_file = "output_data/cities.csv"


this provided a list of cities over 500 and less than 600

with this list a dataframe was created and an api call was made to the OpenWeatherMap url

This helped to create a file with the following information for each city:

cloudinesses.append(response['clouds']['all'])  
countries.append(response['sys']['country'])
dates.append(response['dt'])
humidities.append(response['main']['humidity'])
latitude
longitude
max temperature
wind speeds    

the instructions said to remove cities with hunidity greater than 100 but there were none to delete

A model of weather across world (500+) cities was created using Python script with python library, citypy, and API calls to OpenWeatherMap to retrieve weather data.  

4 scatter plots were then run to demonstrate:  


. latitude versus temperature (max temp)
2. latitude versus humidity
3. latitude versus cloudiness
4. latitude versus wind speed

see plot1.png, plot2.png, plot3.png and plot4.png

I split the results into two files: one northern (latitude > 0), one southern (latitude < 0).

8 scatter charts were created with 4 for the northern latitude and 4 for the southern latitude using linear regression.

1. latitude versus temperature (max temp)
2. latitude versus humidity
3. latitude versus cloudiness
4. latitude versus wind speed

see linearreg1_North.png, linearreg2_North.png, linearreg3_North.png, linearreg4_North.png

Note: Weather Data was pulled 10/24/2022

The r-squared is: 0.7919164615443975 for Max Temp vs Latitude
The r-squared is: 0.04356776881465063 for Humidity vs Latitude
The r-squared is: 0.043042050368342785 for Cloudiness vs Latitude
The r-squared is: 0.020201419250544233 for Wind Speed vs Latitude

see linearreg1_South.png, lianerreg2_South.png, linearreg3_South.png, linearreg4_South.png  

The r-squared is: 0.46043564709913015 for Max Temp vs Latitude
The r-squared is: 0.0049967084909060995 for Humidity vs Latitude
The r-squared is: 0.009003492825842507 for Cloudiness vs Latitude
The r-squared is: 0.036574085868667505 for Wind Speed vs Latitude

th r-squared is worth using between 0 and 1 at around; using percentages > 30 or 40% confirms it may be a valid relationship to compare.
For the Northern Hemisphere this is true for Max Temp vs Latitude 
For the Southern Hemisphere this is true for Max Temp vs Latitude and Humidity vs Latitude.


Using the csv file created with the city information it was then used with Jupyter gmaps and the Google Places API 
A heat map was generated to display humidity for every city from to use Google Maps to create a heat map based on latitude and longitude.
The file was narrowed down to have a max temperature less than 80, no cloudiness and a wind speed less than 10.
Hotels were identified within 5000 meters to the seleted coordinates.

This showed hotels in the United States, Brazil and some of Western Europe as far east as one in India.







