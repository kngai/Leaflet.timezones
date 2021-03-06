# Leaflet.timezones
Overlay timezones on a Leaflet Earth map. 

This is an npm packaged version of https://dj0001.github.io/Leaflet.timezones/. Use the following command to add this package to your project.

```bash
npm install --save @kngai/leaflet.timezones
```

## Demo

https://dj0001.github.io/Leaflet.timezones/

## Usage

Leaflet.timezones extends the GeoJSON class. Adding the sunset to a leaflet popup is as easy as:

    L.timezones.addTo(map);


with timezone popup:

```javascript
L.timezones.bindPopup(function (layer) {
    return layer.feature.properties.time_zone;
}).addTo(map);
```

with worldclock popup:

```javascript
L.timezones.bindPopup(function (layer) {
    return new Date().toLocaleString("en-GB", {timeZone:layer.feature.properties.tz_name1st, timeZoneName:"short"})
}).addTo(map);
```
## License

This project is licensed under the terms of the MIT license.
