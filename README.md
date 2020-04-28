# Visualization-with-GeoPandas-and-GeoPlot

**Creating geovisualization with GeoPandas and GeoPlot like a GIS pro!**

<img src="https://github.com/chelseawmk/Visualization-with-GeoPandas-and-GeoPlot/blob/master/us%20birth%20by%20county%202018.png">

**Data Source:**

* Counties Data from [Kaggle](https://www.kaggle.com/jieyingwu/covid19-us-countylevel-summaries#counties.csv) <br>
* Geospatial Shapefile data from [US Census](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html)

**Steps**
* Prepare and join shape file data with numerical data sources.<br>
* Install Packages<br>
`!pip install git+git://github.com/geopandas/geopandas.git`<br>
`!apt install proj-bin libproj-dev libgeos-dev`<br>
`!pip install git+git://github.com/ResidentMario/geoplot.git`<br>
* Define schema of how many breakdown levels you would like for your map<br>
`scheme = mapclassify.Quantiles(data_column, k=10)`<br>
* Build choropleth map to customize color schemes, lengend, map projection and more.<br>
`gplt.choropleth(county_data, hue=county_data['Unemployment_rate_2018'], scheme=scheme,cmap='coolwarm', figsize=(20, 15),legend=True)`


**Check out more maps within the notebook!**
