Learn-Leaflet-for-Maps

The following steps to do visualize map.

1. Map data can be downloaded from Natural Earth Data
http://www.naturalearthdata.com/downloads/110m-cultural-vectors


2. Data downloaded from Natural Earth Data are in shape format that can be converted into GeoJSON through QGIS tool
http://www.qgis.org/en/site/forusers/download.html

3. Download leaflet http://leafletjs.com/download.html or use a Hosted Version of Leaflet

3. Create basic html code structure

4. Then include leaflet css then js file

5. To Display map using MapBox:
   Create account on MapBox and get access token then paste toke id at accessToken: 'your.mapbox.access.token'
   
   L.tileLayer('https://api.tiles.mapbox.com/v4/{id}/{z}/{x}/{y}.png?access_token={accessToken}', {
    attribution: 'Map data &copy; <a href="http://openstreetmap.org">OpenStreetMap</a> contributors, <a href="http://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery © <a href="http://mapbox.com">Mapbox</a>',
    maxZoom: 18,
    id: 'mapbox.streets',
    accessToken: 'your.mapbox.access.token'
}).addTo(mymap);

To Display map using OpenStreetMap:
var mymap = L.map('mapid').setView([51.505, -0.09], 13);

L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', {
        attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
    }).addTo(mymap);
   
   
