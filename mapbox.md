---
layout: page
title: Mapbox
---

<script src='https://api.mapbox.com/mapbox-gl-js/v2.7.0/mapbox-gl.js'></script>
<link href='https://api.mapbox.com/mapbox-gl-js/v2.7.0/mapbox-gl.css' rel='stylesheet' />


<div id='map' style='width: 400px; height: 300px;'></div>
<script>
mapboxgl.accessToken = 'pk.eyJ1IjoiYmVuamFtaW5jaGFpdCIsImEiOiJjbDBtbjk4b28wZG04M21xMTBiZjk2Mmc0In0.fu809Tdjo0sidzb5O20Vlw';
const map = new mapboxgl.Map({
	container: 'map', // container ID
	style: 'mapbox://styles/mapbox/streets-v11', // style URL
	center: [41.795068, -87.596532], // starting position [lng, lat]
	zoom: 9 // starting zoom
});
</script>
