# python-api-challenge
*This script uses Open Weather API and Google Places API to randomly sample 500+ cities around the world and pulls weather data for analysis. In VacationPy, the same cities are narrowed down by weather conditions and Google Places API is used to search for nearby hotels, then create a heatmap using gmaps with compiled data.*
*In order to run, you will need to configure your own api keys for both and import from a config.py file*

# Part I - WeatherPy 
## Summary Plots
![lat_vs_temp_chart.png](output_data/lat_vs_temp_chart.png?raw=true "Title")

This plot illustrates that as latitude approaches the equator (latitude of 0 degrees), temperature increases. As latitudes increase into the northern hemisphere, specifically (denoted by a positive value of latitude), temperatures decrease. Especially as the northern hemisphere is currently experience winter, this makes logical sense. 


![lat_vs_humidity_chart.png](output_data/lat_vs_humidity_chart.png?raw=true "Title")

This plot illustrates that there are a wide range of humidities at any given latitude. Other factors (such as latitude, cloudiness, or max temp) may be more beneficial in predicting humidity of a specific location. 

![lat_vs_cloud_chart.png](output_data/lat_vs_cloud_chart.png?raw=true "Title")

This plot is similar to latitude vs. humidity in that there is a wide range of cloudiness at any given latitude.

![lat_vs_wind_chart.png](output_data/lat_vs_wind_chart.png?raw=true "Title")

This plot shows a wide range of wind speeds at any given latitude, but the majority of the wind speeds fall between 0 and 15 mph. Wind speeds above 15 mph are more rare, and these locations could be analyzed to be outliers or compared using other factors. 

## Plots by Hemisphere

### Temperature
| Northern Hemisphere | Southern Hemisphere |
| ------------------- | ------------------- |
| ![north_lat_temp_regression.png](output_data/north_lat_temp_regression.png?raw=true "Title") | ![south_lat_temp_regression.png](output_data/south_lat_temp_regression.png?raw=true "Title")|
 
 In both hemispheres, as latitudes approach the equator (latitude value of 0), max temperature increases.

### Humidity
| Northern Hemisphere | Southern Hemisphere |
| ------------------- | ------------------- |
| ![north_lat_hum_regression.png](output_data/north_lat_hum_regression.png?raw=true "Title") | ![south_lat_hum_regression.png](output_data/south_lat_hum_regression.png?raw=true "Title")|

In the northern hemisphere, as latitude increases, humidity increases but not with a strong correlation. In the southern hemisphere, the closer to the equator a location, the highter the humidity. Intuitively, one would think that that humidity increases with proximity to the equator. The high humidity in the northern hemisphere at greater latitudes is counterintuitive. This could be baesd on seasons and a higher deal of moisture in the air due to cloud cover, rain, or snowfall weather patterns during the winter months.

### Cloudiness
| Northern Hemisphere | Southern Hemisphere |
| ------------------- | ------------------- |
| ![north_lat_cloud_regression.png](output_data/north_lat_cloud_regression.png?raw=true "Title") | ![south_lat_cloud_regression.png](output_data/south_lat_cloud_regression.png?raw=true "Title")|

Based on these figures, cloudiness (%) has a similar relationship to latitude as that of humidity and latitude. Further analysis and understanding of differences between and interconnectedness of cloud cover and humidity would be warranted. 

### Wind Speed
| Northern Hemisphere | Southern Hemisphere |
| ------------------- | ------------------- |
| ![north_lat_wind_regression.png](output_data/north_lat_wind_regression.png?raw=true "Title") | ![south_lat_wind_regression.png](output_data/south_lat_wind_regression.png?raw=true "Title")|

There appears to be a slight correlation between latitude and wind speed. In general, as latitudes approach the equator, wind speed decreases. 



## Additional Analysis

* As mentioned above, latitudes closer to the equator in this model tend to have lower wind speeds. It would be an interesting analysis to compare wind speed with other values such as cloudiness, humidity, or minimum temperatures to find any possible correlation. One thing to note is that latitudes closer to the equator would tend to have smaller swings in temperature on any given day. Wind speeds increase with greater temperature differences, so it makes sense that cities farther from the equator would have a greater swing in teperature as well as wind speed. Further analysis could give more detail. 

* In both hemispheres, as latitudes approach the equator (latitude value of 0), max temperature increases. There is a strong correlation between latitude and temperature in the southern hemisphere, and a slightly stronger correlation in the northern hemisphere. The sharper decrease in maximum temperature in the northern hemisphere could be due to the fact that it is currently winter in the north and summer in the south. 

* The data denoting latitude vs humidity shows a great number of cities in this sample being at a relatively high humidity, but with more clustering of data in the northern hemisphere. This could be affected by the number of cities in this sample in the northern hemisphere, by the time of year, or there could be less cities populating the southern hemisphere overall, based on loctation of inhabitable land. 

# Part II - VacationPy 
