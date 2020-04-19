<template lang="html">
  <div>
    <ul>
      <list-item v-for="(image, index) in images" :image="image" :key="index"></list-item>
    </ul>
  </div>

</template>

<script>
import ListItem from './ListItem.vue';

export default {
  name: 'images-list',
  props: ['images'],
  components: {
    "list-item": ListItem
  }
}
</script>

<style>

</style>
