# GeoHash
##Step 1: Load the Dataframe (csv file using pandas)

##Step 2: Convert the data to GeoDataFrame using geopandas library.

##Step 3: Find the geohash values using geohash library

###installing
  npm install ngeohash
 
###Basic Methods 

  geohash.encode (latitude, longitude, precision=9)
  
  Encode a pair of latitude and longitude values into a geohash. The third argument is optional, you can specify a length of this hash string, which also affects the precision of the geohash.
  
  geohash.decode (hashstring)
  
  Decode a hash string into pair of latitude and longitude values. A javascript object is returned with latitude and longitude keys.
  
  geohash.decode_bbox (hashstring)
  
  Decode hashstring into a bounding box that matches it. Data is returned as a four-element array: [minlat, minlon, maxlat, maxlon].
  
##Step 4: Find corrseponding polygon. (Using polygon-geohasher)
 
 ###Installing
 
  Linux users can get Polygon Geohasher from the Python Package Index with pip (8+):
  
  $ pip install polygon-geohasher    
 
 ###Use
  
  geohash_to_polygon(geohash):
 
 This function receives a geohash and returns a Shapely's Polygon.
  
  geohashes_to_polygon(geohashes):
 
 This function receives a set of geohashes and returns a Shapely's Polygon or MultiPolygon.

##Step 5: Use folium to construct the layer on map.
