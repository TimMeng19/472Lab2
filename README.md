# 472Lab1 - Haotian Meng



## 1. A screenshot of the web map:
[logo]: https://github.com/TimMeng19/472lab2/blob/main/screenshot.png "Screenshot of the map"
![alt text][logo]


##  2. The Github Pages link to the web map



The Mapbox style file can be found in the main page of this repo

## 3. The Reflective Analysis

The Presidential Election of the United States is one of the most influential and famous political events. Although I am not an American, I always like to follow up on the election progress and check out the result, and this is mainly because I like to look at election-related choropleth maps and decode information geographically. Analyzing the election result by visualizing the election result can reveal insights from the spatial aspect for each state, region and city. In this assignment, the purpose is to examine the total votes change in the US Presidential Election from 2000 to 2016 at county level. 

This web-map is designed for presidential campaign managers and presidential candidate, since this map can reflect whether counties in a region experience increases or not in total votes and this information can be considered in their future campaigns. The main dataset, County Presidential Election Returns 2000-2016, was retrieved from Harvard Dataverse, a public open data source. Then, this dataset was spatially joined with all US counties in ArcGIS Pro, the change of total vote for each county (Total vote in 2016 divided by Total vote in 2000) was also being calculated in ArcGIS Pro. It should be noted that the electoral college in the state of Alaska is a different system than the counties system there, therefore all electoral colleges are merged together and represent Alaska as a whole. After the initial data standardization and modification, this modified polygon dataset was uploaded into Mapbox Studio and further styled cartographically for better visualization. Similar to the previous assignment, I used The Guide to Map Design written by Amy Lee for customizing the visual hierarchy and other cartographic aspects. I used the Monochrome style base-map and hide road, building and natural layers since these are not the focus in this web-map. For the total vote layer, the change of total vote was classified in to six groups, and a diverging color scheme was applied to the dataset. The reason I chose a diverging color scheme is because the change can be either smaller than 1 or greater than 1, and representing two different status (experiencing an increase or decrease) for a county. Therefore, a diverging color scheme can reflect this difference effectively and straightforwardly. Comparing to the last assignment, fewer changes were made via Mapbox Studio, while more interactivity was added to the map through programming in Mapbox GL JS.

In Atom.io, I further enhanced my web-map and add interactivity to it. Firstly, basic elements including a legend, a title and popup windows for every county were added for this map to provide basic knowledge for the viewers to understand this map. Also, I retrieved two APIs from Mapbox, which are an address search bar and a geolocate button. Both of these two features are located at the top-right corner of the map, and the reason I decided to add them is because they enable users to easily check out the layer and result at their current location or anywhere they are interested in. Other than these features, I spent most of my energy on implementing a filter list (the left sidebar) for all the input data from the layer. Basically, what this filter does is it takes user input (name of a county) then find and filter out one or more counties that matches this input on both the map and the list. After that, the map can also zoom to the location of a county if users click on its name. Lastly, the reset button next to the filter sidebar can always take users back to the original view.

Although the interactive filter mentioned above is working, many bugs still exist. For example, after doing a filter, if you use your mouse to pan over the map, the list “forgets” the data for the filtered-out counties. This means that data cannot be loaded correctly after that and users have to reboot the page to reset it. I tried to resolve these bugs but only succeed on a few of them. Beside resolve the bugs, one aspect I can further enhance the map is to add an interactive line chart showing the change of total vote from 2000 to 2016. This is definitely a much better feature than only the popups and plain numbers. In summary, there are still many places to improve for this map to make it more useful.


## 4. Coding resources

Locate the user:
https://docs.mapbox.com/mapbox-gl-js/example/locate-user/
Center the map on a clicked symbol:
https://docs.mapbox.com/mapbox-gl-js/example/center-on-symbol/
Fit to the bounds of a LineString:
https://docs.mapbox.com/mapbox-gl-js/example/zoomto-linestring/
API Reference:
https://docs.mapbox.com/mapbox-gl-js/api/
Display a popup on click:
https://docs.mapbox.com/mapbox-gl-js/example/popup-on-click/
Dynamic charts:
https://labs.mapbox.com/education/impact-tools/line-charts/
Filter features within map view:
https://docs.mapbox.com/mapbox-gl-js/example/filter-features-within-map-view/
