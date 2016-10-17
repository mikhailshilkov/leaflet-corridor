leaflet-corridor
================
Renders a polyline with width fixed in meters, not in pixels. This means 
that the line width changes whenever zoom level changes. Handy to denote 
geographic corridors: ranges of specified width around a polyline.

![Leaflet-corridor screenshot](http://mikhail.io/2016/10/leaflet-corridor/leaflet-corridor.png)

*Tested with Leaflet 0.7.1 or newer*

## Demo
[Live demo](http://mikhail.io/demos/leaflet-corridor/)

## Getting started
Using leaflet-corridor plugin is very easy.
### Usage
* Download and place the `leaflet-corridor.js` file in your project.
* Link javascript file in your HTML document:
```html
<script src="...path-to-files.../leaflet-corridor.js"></script>
```
* Then use in simple way in javascript file:
```javascript
// Create polyline coordinates
var coords = [
  L.latLng(-44.696476, 169.13693),
  L.latLng(-44.69764, 169.134602)
  // ...
];

// Define corridor options including width
var options = { 
  corridor: 1000, // meters
  className: 'route-corridor' 
};

// Create a corridor and add to the map
var corridor = L.corridor(coords, options);
map.fitBounds(corridor.getBounds());
map.addLayer(corridor);
```

### Parameters
| Parameter         | Description
| ----------------- | ---------------------- 
| latlngs           | Array of L.latLng to define polyline coordinates
| options.corridor  | Width of the corridor in meters
| options.*         | Options for polyline rendering, exactly same as in L.polyline

### License

**leaflet-corridor** is free software, and may be redistributed under the MIT-LICENSE.