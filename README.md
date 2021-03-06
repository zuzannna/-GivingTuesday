#Giving Tuesday DataKind Dive

**Transaction-level data can give us consumer insights into giving patterns and giving motivations.  It can  provide insights to organizations seeking funds and help create measures of giving - such as an increase in amount or people giving by day or by year.**  

I dove into donation transaction records provided by big companies such as **Paypal** and combined them with **US census data** (freely available) and **ZIP code shapefiles** (geospatial representation of ZIP codes) to create an interactive map of individual donors who contributed less than $200.

When analyzing individual donations in the context of the whole country it is important to look at the normalized values - adjusted by the median income in the area. This way by visual inspection of the map it is possible to identify the areas which are more likely to donate significant portions of their income. 

This is why I in the analysis below I used the following normalization method:

![normalizing](normalizing.png)

**purpose:** provide a map of small donors normalized by the income to direct marketing campaign more efficiently, especially outside of big cities.

**data:** I used a subset of transactions data narrowed down to 2016 by executing "cat donations_post_gt.csv | grep 2016 >> donations_post_gt_2016.csv" in the Terminal. 

**tools:** numpy, pandas, matplotlib, GeoPandas


Deliverable is the code and the following map, which can be accessed at: https://zuzanna.carto.com/viz/999bdc1a-01c1-11e7-9bf4-0e3ff518bd15/map.  

![map_image](map_image.png)

#Insights:
Interestingly, when we look at adjusted donation amounts we see that big cities no longer dominate the giving drive. For example, there are ZIP codes areas in south Texas, Utah, Montana and Idaho which donate as much or more than urbanized centers on the West and East Coast. By hovering over the map we can inspect specific zip codes, the number of households within the area and the total amount of donations.