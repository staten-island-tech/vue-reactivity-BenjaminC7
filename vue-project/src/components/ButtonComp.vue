<template>
  <button><slot></slot></button>
</template>

<script>
export default {
  name: "ButtonComp",
};
</script>

<style lang="scss" scoped>
button {
  width: 200px;
  font-size: 30px;
  border-radius: 20px;
  border: none;
  background-color: red;
  color: white;
}
</style>
