<template>
    <h3>{{ name }}</h3>
    <img id="img" v-bind:src="image" alt="" />
    <p id="price">Price: ${{ price }}</p>
</template>

<script>
export default {
  name: "CardComponent",
  props: {
    name: String,
    price: Number,
    image: String,
  },
};
</script>

<style></style>
