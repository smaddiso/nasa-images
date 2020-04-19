<template lang="html">
  <li v-on:click="handleClick">{{image[0]}}</li>
</template>

<script>
import {eventBus} from '../main.js';

export default {
  name: 'list-item',
  props: ['image'],
  methods: {
    handleClick(){
      eventBus.$emit('image-selected', this.image)
    }
  }
}
</script>

<style>

</style>
