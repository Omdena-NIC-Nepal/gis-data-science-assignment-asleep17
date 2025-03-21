# GIS_Data_Science
## Assignment: GIS Data Science for Climate in Nepal
### Objective:
- The objective of this assignment is to assess your understanding and practical skills in GIS Data Science, specifically focusing on climate data analysis for Nepal. You will be required to perform data reading, visualization, and exploratory data analysis (EDA) tasks using Python.

### Steps to Complete the Assignment:
#### Setup Instructions:

- Clone the repository from GitHub Classroom.
- Ensure Python environment is set up with necessary libraries (e.g., pandas, geopandas, matplotlib, seaborn).
#### Data Collection and Preparation:

- Data Source: https://opendatanepal.com/dataset/district-wise-daily-climate-data-for-nepal
- Data Reading: Climate_data is read using pandas.read_csv()
-Data Preprocessing:
    * Latitude and longitude coordinates are used to create `shapely.Point` geometries.
    * Coordinate Reference System (CRS) is set to EPSG:4326 for both GeoDataFrames. The boundary file is reprojected if necessary.
    * District names are standardized (lowercase, stripped spaces) and inconsistencies are addressed using `.replace()`.
    * A spatial join is performed using `gpd.sjoin` to combine climate and boundary data.
    * Climate data is aggregated by district using `groupby()` to calcu
### Data Visualization:

- Task: Visualize the GIS data to explore climate patterns in Nepal.
#### Required Visualizations: Include at least:
-Boxplots for Outlier Detection:
    * Boxplots of precipitation and temperature are generated to identify potential outliers in the data.
    * This helps in understanding the distribution and identifying extreme values.
-Scatter Plot of Temperature vs. Precipitation:
    * A scatter plot is created to explore the relationship between temperature and precipitation.
    * This helps in understanding the correlation and patterns between these climate variables.
-Boxplot of Temperature Yearly:
    * Boxplots are generated to show the distribution of temperature values for each year.
    * This visualization helps to identify yearly variations and potential trends.
-Temperature Trend Map:
    * A map showing the spatial trend of temperature is generated.
    * This map visualizes how temperature changes spatially across Nepal.
-Precipitation Trend Map:
    * A map showing the spatial trend of precipitation is generated.
    * This map visualizes how precipitation changes spatially across Nepal.
- Any additional relevant visualizations that help interpret climate data.
#### Exploratory Data Analysis (EDA):
## Exploratory Data Analysis (EDA)
   We loaded the climate data and found variables like Temperature, Precipitation, Humidity, and Wind Speed. We then looked at basic statistics to understand the data better.

   The average temperature was 15.8°C, but it ranged from -17.81°C to 35.59°C, showing big differences across Nepal. Rainfall varied a lot too, with an average of 68.92 mm but some areas getting up to 641.84 mm. Humidity and wind speed showed moderate changes.

   We used boxplots to find extreme values in rainfall and temperature, and scatter plots to see if temperature and rainfall were related (they weren't strongly). Maps showed where temperature and rainfall were highest and lowest. We also looked at how temperature changed each year.

   During our analysis, we found some data points were outside of Nepal's districts, which we need to fix. We also saw some very high rainfall values that might be errors.

   In short, Nepal's climate changes a lot across the country. We need to check some data points and fix some errors before doing more analysis.

##### Tasks:
-Compute basic statistics:
    * Mean, median, min, and max values of precipitation and temperature are calculated using `.describe()`.
-Identify trends and patterns:
    * Spatial patterns of climate variables are analyzed using choropleth maps.
-Observations and Insights:
    * District name discrepancies were a significant challenge, requiring data cleaning and standardization.
    * Null values in precipitation data indicate missing data for some districts.
    * `nan` values in the district column after the spatial join, show that some points were outside of the district boundries.
    * Choropleth maps show the spatial distribution of climate variables.
    * The spatial join was verified by plotting the points over the district polygons.
    * Mean temperature and precipitation values, and ranges were observed.
