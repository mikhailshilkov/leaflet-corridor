leaflet-corridor
================
Renders a polyline with width fixed in meters, not in pixels. This means 
that the line width changes whenever zoom level changes. Handy to denote 
geographic corridors: ranges of specified width around a polyline.

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

// Define corridor options
var width = 1000; // meters
var options = { className: 'route-corridor' };

// Create a corridor and add to the map
var line = L.corridor(coords, width, options);
map.fitBounds(line.getBounds());
map.addLayer(line);
```

### Parameters
| Parameter       | Description
| --------------- | ---------------------- 
| latlngs         | Array of L.latLng to define polyline coordinates
| corridor        | Width of corridor in meters
| options         | Options for polyline rendering, exactly same as in L.polyline

### License

**leaflet-corridor** is free software, and may be redistributed under the MIT-LICENSE.