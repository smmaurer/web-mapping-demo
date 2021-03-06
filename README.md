Tools for creating interactive online maps
-----

Guest lecture for [CP 255 Urban Informatics](https://github.com/gboeing/cp255-materials)  
UC Berkeley  
November 4, 2015

[Download slides](http://smmaurer.github.io/web-mapping-demo/Maurer%20web%20mapping%20slides.pdf)  
[Download zipped demo files](http://smmaurer.github.io/web-mapping-demo/web-mapping-demo-files.zip)


#### Examples from lecture

* San Francisco Planning Department - Active Permits  
  http://www.sf-planning.org/index.aspx?page=2575

* Transit & Trails - Bay Area Trailheads  
  http://www.transitandtrails.org/find/trailheads

* Urban Displacement - Bay Area Displacement Typologies  
  http://www.urbandisplacement.org/map

* Google Maps  
  http://maps.google.com/

* Hill Mapper San Francisco  
  http://hillmapper.com/

* Eric Fischer - Mapping six billion tweets  
  https://www.mapbox.com/blog/twitter-map-every-tweet/

* Bert Spaan - All Buildings in the Netherlands  
  http://code.waag.org/buildings/

* Fall Foliage Prediction Map  
  http://smokymountains.com/fall-foliage-map/


## Demo instructions

In `awesome_map.html`, we'll use the [Leaflet](http://leafletjs.com) Javascript library to overlay the data from `dataset.js` on top of basemap layers from [Mapbox.com](http://mapbox.com)


#### First, create some point markers for the overlay

* Go to [GeoJSON.io](http://geojson.io), zoom into the Bay Area, and use the drawing tools to create some point markers. You'll see JSON code appear in the right-hand pane

* Let's add a data field for marker labels. Go to the "Table" tab, create a new column, and call it `name`, and fill in the rows

* When you're done creating markers, open `dataset.js` in a text editor, select all the JSON code from the right-hand column of the web page, and copy/paste it into the text file below the first line


#### Next, choose some basemap layers

* Go to [Mapbox.com](http://mapbox.com), sign in, and click on the "Projects" folder in the upper right

* Open `awesome_map.html` in a text editor, and copy/paste your access token id from the top of the Mapbox projects page to line 74 of the code ([see line here](https://github.com/smmaurer/web-mapping-demo/blob/master/awesome_map.html#L74))

* Open up two new map projects (in separate browser tabs), and take a look at the different basemap options. We'll use one normal basemap and one of the crazier ones

* For the first map, go to the "Project" tab, save it, and copy/paste the map id to line 75 of `awesome_map.html` ([see line here](https://github.com/smmaurer/web-mapping-demo/blob/master/awesome_map.html#L75))

* Do the same for the second map, in the following line


#### Now we can look at the map and adjust the code

* Open `awesome_map.html` in a web browser. You should see a basemap and the marker overlay, with marker names appearing when you click on them

* Try out some of the buttons, which demonstrate ways you can interact with map objects that have been drawn in the browser

* It will be helpful to open up the error console to diagnose potential Javascript bugs
  * In Safari, go to Safari > Preferences > Advanced, and turn on the developer menu. Then go to Develop > Show Error Console
  * In Chrome, go to View > Developer > Javascript Console

* Go through the web page code in a text editor, and see if you can fix the buttons that are missing function definitions!

* The [Leaflet](http://leafletjs.com) code reference will be helpful: http://leafletjs.com/reference.html


#### Additional resources

* [Mapshaper.org](http://mapshaper.org) lets you view shapefile-format map data in a web browser, and convert it to geojson format, which can be handy if you don't have GIS software installed

* CartoDB has a new scheme for creating web maps with non-Mercator projections, which looks neat: http://blog.cartodb.com/free-your-maps-web-mercator/

* Mapbox is building a Javascript library for performing GIS-type processing operations (like buffers and contours) in the browser. You could create some cool interactive maps with this: https://www.mapbox.com/blog/turf-gis-for-web-maps/