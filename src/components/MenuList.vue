<template>
  <div>
    <!-- <h1>Menu List</h1> -->
    <menu-item v-for="item in items" :key="item.id" :item="item"></menu-item>
  </div>
</template>

<script>
import MenuItem from './MenuItem.vue';

export default {
  components: {
    MenuItem,
  },
  props: ['items']
}
</script>

<style scoped>
div {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 10px;
  justify-content: center;
  align-items: center;
}
h1 {
  text-align: center;
}
</style>
