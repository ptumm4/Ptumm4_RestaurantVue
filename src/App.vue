<template>
  <div id="app">
    <menu-manager></menu-manager>
  </div>
</template>

<script>
import MenuManager from './components/MenuManager.vue';

export default {
  components: {
    MenuManager,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #0a0a0a;
  margin: 50px;
  background-color: antiquewhite;
}
</style>
