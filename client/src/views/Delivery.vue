<template>
  <div class="delivery">
    <h1>Delivery Tracking</h1>
  </div>
</template>
<script>
console.log('loading map...');
  // container IS finished rendering to the DOM
    console.log('map loaded.');
    var mapboxgl = require('mapbox-gl/dist/mapbox-gl.js');
    mapboxgl.accessToken = 'pk.eyJ1IjoiYXJrY2xvdWR0ZWNoIiwiYSI6ImNqdGI1ejZvcDBpZWgzeWw2bTg5cHNsdW4ifQ.0AaN6PAybDuhZcHZgGKFXg';
    const map = new mapboxgl.Map({
    container: 'puffymap',
    style: 'mapbox://styles/arkcloudtech/cjtb89hli1w3o1fpm6kuwa5je',
    center: [-73.991866, 40.727021],
    zoom: 13.2
    });


var marker = new mapboxgl.Marker()
.setLngLat([-21.9270884, 64.1436456])
.addTo(map);

    map.on('click', function(e) {

    var popup = new mapboxgl.Popup({ offset: [0, -15] })
        .setLngLat(feature.geometry.coordinates)
        .setHTML('<h3>' + feature.properties.title + '</h3><p>' + feature.properties.description + '</p>')
        .setLngLat(feature.geometry.coordinates)
        .addTo(map);
        
    });
</script>