# BVU Campus01
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BVIEER MAP1</title>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.3/dist/leaflet.css" integrity="sha256-kLaT2GOSpHechhsozzB+flnD+zUyjE2LlfWPgU04xyI=" crossorigin="" />
    <script src="https://unpkg.com/leaflet@1.9.3/dist/leaflet.js" integrity="sha256-WBkoXOwTeyKclOHuWtc+i2uENFpDZ9YPdf5Hf+D7ewM=" crossorigin=""></script>
</head>
<style>
    #map {
        height: 100vh;
        width: 100vw;
    }
</style>
<div id="map"></div>
<body>
    <script>
        let map =L.map("map").setView([18.460448532213547, 73.85224714906508],17)
        let osm =  L.tileLayer('https://{s}.tile.openstreetmap.fr/osmfr/{z}/{x}/{y}.png', {
            maxZoom: 20,
            attribution: '&copy; OpenStreetMap France | &copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
        });
    osm.addTo(map)
        let bvieerMarker = L.marker([18.46106031852471, 73.85268955336483]).addTo(map);
        let FineArts = L.marker([18.4597894864192, 73.85459304913844]).addTo(map);
        let groundMarker = L.marker([18.460009551529193, 73.85439833188997]).addTo(map);
        let Cinematography = L.marker([18.459924802738186, 73.85338784669811]).addTo(map);
        let BVIEER = L.marker([18.46026693265296, 73.85215812558725]).addTo(map).addTo(map);

        bvieerMarker.bindPopup("Hotel Management Institute");
        bvieerMarker.bindTooltip("click for name")

        groundMarker.bindPopup("Institute of physiotherapy");
        groundMarker.bindTooltip("click for name")
        
        FineArts.bindPopup("FineArts");
        FineArts.bindTooltip("click for name")

        Cinematography.bindPopup("Cinematography");
        Cinematography.bindTooltip("click for name")

        BVIEER.bindPopup(`
        <h1>Bharati Vidyapeeth Institute of Environment Education and Research</h1>
        <img src="https://lh5.googleusercontent.com/p/AF1QipMwbk7uKK--76xP3VgHP2q5E7rLYPezTGiTBzIY=w200-h240-k-no" alt="BVIEER">
        `);
        BVIEER.bindTooltip("click for name")


        let long_lat = [[18.457616265383386, 73.8531836519893], [18.456822668483213, 73.85353281167117], [18.456736925466465, 73.85352966585683], [18.456076764388698, 73.85361002606308], [18.456110686606117, 73.854703905994], [18.454608179861534, 73.85496322551293], [18.454602978204907, 73.85597556698312], [18.455147218126395, 73.8559387181748], [18.455182614179392, 73.85645208979825], [18.456276455392015, 73.85646711262147], [18.456419149201107, 73.85728139685162], [18.456979158515633, 73.85728647751502], [18.456987537107935, 73.8581684067041], [18.457973031089377, 73.85805095903602], [18.460020007702166, 73.85785783313547], [18.46015823315772, 73.85668416607987], [18.46042529909848, 73.85666652547434], [18.460389220563183, 73.8535421761378], [18.460938005617315, 73.85231739380419], [18.459914529201306, 73.85116846559846], [18.459431643475718, 73.85125016027578], [18.458887467803237, 73.85088976071216], [18.458806733923634, 73.85159205419855], [18.45736315998266, 73.85174337454981]];
        let bvieerArea = L.polygon(long_lat, {color:'black'}).addTo(map);
        bvieerArea.bindPopup("BVU CAMPUS")
</script>
</body>
</html>
