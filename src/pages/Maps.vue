<template>
    <card class="card-map" title="Google Maps">
      <div class="map">
        <div id="map"></div>
      </div>
    </card>
</template>
<script>
export default {
  mounted() {
    var myLatlng = new window.google.maps.LatLng(-6.2167798, 106.682188);
    var mapOptions = {
      zoom: 16,
      center: myLatlng,
      scrollwheel: false, 
    };
    var map = new window.google.maps.Map(
      document.getElementById("map"),
      mapOptions
    );

    var marker = new window.google.maps.Marker({
      position: myLatlng,
      title: "This is my house!!"
    });

    marker.setMap(map);
  }
};
</script>
<style>
</style>
