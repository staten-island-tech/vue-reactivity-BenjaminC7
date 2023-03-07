<template>
  <div>
    <h1>wow</h1>
    <p>This is a test</p>
  </div>
</template>

<script>
export default {
  name: "CoolCard",
  props: {
    animal: Object,
  },
};
</script>

<style scoped>
div {
  height: 500px;
  width: 300px;
  background-color: red;
  color: white;
}
h1 {
  font-size: 32px;
}
</style>
