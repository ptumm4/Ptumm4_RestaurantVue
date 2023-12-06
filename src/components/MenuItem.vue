<template>
  <div>
    <h2>{{ item.name }}</h2>
    <p>{{ item.description }}</p>
    <p>{{ item.price }}</p>
  </div>
</template>

<script>
export default {
  props: ['item']
}
</script>

<style scoped>
div {
  border: 1px solid #ddd;
  padding: 10px;
  margin: 10px;
  text-align: center;
  background-color: azure;
  border-radius: 10%;
}
</style>
