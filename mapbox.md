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
	center: [-74.5, 40], // starting position [lng, lat]
	zoom: 9 // starting zoom
});
</script>

<div id='maptwo' style='width: 400px; height: 300px;'></div>
<script>
mapboxgl.accessToken = 'pk.eyJ1IjoiYmVuamFtaW5jaGFpdCIsImEiOiJjbDBtbjk4b28wZG04M21xMTBiZjk2Mmc0In0.fu809Tdjo0sidzb5O20Vlw';
const maptwo = new mapboxgl.Map({
	container: 'maptwo', // container ID
	style: MAPBOX_STYLE_URL, // style URL
	center: [-87.596532, 41.795068], // starting position [lng, lat]
	zoom: 12 // starting zoom
});

let MAPBOX_STYLE_URL : String = {
    if UITraitCollection.current.userInterfaceStyle == .dark {
        return "mapbox://styles/mapbox/dark-v10" 
    }
    else {
       return "mapbox://styles/mapbox/light-v10" 
    }
}()

struct ContentView: View {

    @Environment(\.colorScheme) var colorScheme

    var mapboxStyleURL: String {
        "mapbox://styles/custom" + (colorScheme == .dark ? "Dark" : "Light") + "ModeUrl" 
    }

    var body: some View {
        Text(mapboxStyleURL)
    }
}

</script>
