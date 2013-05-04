Leaflet.Control.Search
============

#What
A leaflet control that search markers location by property
with ajax/jsonp autocomplete feature and json fields complete re-mapping

Tested in Leaflet 0.5.1

#How
Insert leaflet-search.css styles to your css page

Adding the search control to the map:

```
map.addControl( new L.Control.Search({layer: searchLayer}) );
//searchLayer if a L.LayerGroup contains searched markers
```

other examples:
```
map.addControl( new L.Control.Search({url: 'search.php?q={s}', jsonpParam: 'callback'}) );
//searchJsonpUrl is jsonp service for retrieve elements locations

map.addControl( new L.Control.Search({
		url: 'http://nominatim.openstreetmap.org/search?format=json&q={s}',
		jsonpParam: 'json_callback',
		propertyName: 'display_name',
		propertyLoc: ['lat','lon']
	}) );
//implements Geocode Searching using OSM API
```

#Where
Source code:
[github](https://github.com/stefanocudini/leaflet-search)
[bitbucket](https://bitbucket.org/zakis_/leaflet-search)

Demos:
[labs.easyblog.it/maps/leaflet-search](http://labs.easyblog.it/maps/leaflet-search/)

