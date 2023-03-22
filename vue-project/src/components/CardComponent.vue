<template>
  <div class="item">
    <h3>{{ name }}</h3>
    <img id="img" v-bind:src="image" alt="" />
    <p id="price">Price: {{ price }}</p>
    <button id="purchaseBtn">Purchase</button>
  </div>
</template>

<script>
export default {
  name: "CardComponent",
  props: {
    name: String,
    price: String,
    image: String,
  },
};
</script>

<style lang="scss"></style>
