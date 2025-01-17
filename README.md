# vue3-leaflet-googlemutant

This is a [googlemutant plugin](https://gitlab.com/IvanSanchez/Leaflet.GridLayer.GoogleMutant) extension for [vue3-leaflet package](https://github.com/KoRiGaN/vue3Leaflet)

## Install

    npm install --save vue3-leaflet-googlemutant vue3-leaflet leaflet leaflet.gridlayer.googlemutant

## Demo

    git clone git@github.com:jperelli/vue3-leaflet-googlemutant.git
    cd vue3-leaflet-googlemutant
    yarn
    yarn example

    # or alternatively using npm
    npm install
    npm run example

Then you should be able to navigate with your browser and see the demo in http://localhost:4000/

You can see the demo code in the file [example.vue](example.vue)

## Usage

### on &lt;template&gt; add

something like this

    <v-map :zoom=10 :center="initialLocation">
      <v-icondefault :image-path="'/statics/leafletImages/'"></v-icondefault>
      <v-tilelayer url="http://{s}.tile.osm.org/{z}/{x}/{y}.png"></v-tilelayer>
      <v-tilelayer-googlemutant apikey="YOUR_API_KEY" lang="YOUR_LANG" region="YOUR_REGION" :options="googlemutantoptionsobject">
      </v-tilelayer-googlemutant>
    </v-map>

For available languages and regions, refer to Google Maps documentation on [localizing the map](https://developers.google.com/maps/documentation/javascript/localization).

### on &lt;script&gt; add

#### option 1

In the same template file, at `<script>` part, this will make the component available only to the template in this file

    import vue3LeafletGoogleMutant from 'vue3-leaflet-googlemutant'
    ...
    export default {
      ...
      components: {
        'v-tilelayer-googlemutant': vue3LeafletGoogleMutant
        ...
      },
      ...
    }

#### option 2

At main Vue configuration, this will make the component available to all templates in your app

    import Vue from 'vue'
    import vue3LeafletGoogleMutant from 'vue3-leaflet-googlemutant'
    ...
    Vue.component('v-tilelayer-googlemutant', vue3LeafletGoogleMutant)

## Develop and build

    npm install
    npm run build

## Author

[Julián Perelli](https://jperelli.com.ar/)

## License

MIT
