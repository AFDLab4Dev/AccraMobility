# AccraMobility

## Context

On this repository you will find all resources available on the project Accra Mobility (previously Accra Mobile) led by Municipality of Accra and AFD (Agence Française de Développement).

More information about the project is available on beta.dataspace.fr/accramobility.

Our friends from JungleBus have made a map, you can find it here: http://junglebus.io/accra/#13/5.5781/-0.2432. Check http://wiki.openstreetmap.org/wiki/AccraMobile3 for more details on methodology :) ! 

## How to get raw data (geojson) ?

Lines have been mapped on OpenStreetMap. The easiest way to get the most up-do-date geojson of Accra's trotro lines is to query them directyly on OpenStreetMap. 

How to do it ?

A simple web-app, called [overpass-turbo](http://overpass-turbo.eu/), allow to do simple queries on OpenStreetMap and download as a geojson all the data.

You should have to go on http://overpass-turbo.eu/ and copy-paste the following block:

```
[out:json];

{{geocodeArea:Greater Accra Region}}->.searchArea;

(
  relation["type"="route"]["bus"="unofficial"](area.searchArea); 
);
out body;
>;
out skel qt;
```

You can also directly click on the following link: https://overpass-turbo.eu/s/tIr

A few other useful requests :
* if you just want the stops : https://overpass-turbo.eu/s/tIs
* if you just want line metadata : https://overpass-turbo.eu/s/tIq

## Resources available

- Map (in SVG)
- GTFS Data
- Research papers

