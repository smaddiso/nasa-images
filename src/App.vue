<template>
  <div>
    <h1>NASA Images</h1>
    <div>
      <images-list :images='images'></images-list>
    </div>
  </div>
</template>

<script>
import ImagesList from './components/ImagesList.vue';
import {eventBus} from './main.js';

export default {
  name: 'App',
  data(){
    return {
      images: []
    };
  },
  mounted(){
    fetch('https://api.nasa.gov/mars-photos/api/v1/rovers/curiosity/photos?sol=1000&api_key=DEMO_KEY')
    .then(result => result.json())
    .then(images => this.images = images)
  },
  components: {
    "images-list": ImagesList
  }
}

</script>

<style>

</style>
