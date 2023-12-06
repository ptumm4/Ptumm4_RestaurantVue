<template>
  <div>
    <h1>Restaurant Menu</h1>
    <button @click="fetchData">Fetch Data</button>
    <menu-list v-if="items.length" :items="items"></menu-list>
  </div>
</template>

<script>
import MenuList from './MenuList.vue';
import axios from 'axios';

export default {
  components: {
    MenuList,
  },
  data() {
    return {
      items: [],
    };
  },
  methods: {
    fetchData() {
      axios.get('https://ptumm4restaurantrender.onrender.com/api')
        .then(response => {
          this.items = response.data;
        })
        .catch(error => {
          console.error('Error fetching data:', error);
        });
    },
  },
};
</script>

<style scoped>
div {
  text-align: center;
}
button {
  margin: 50px;
  padding: 10px;
  background-color: #4caf50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>
