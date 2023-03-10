<template>
  <div>
    <h1 v-if="graduated">{{ student }}</h1>
    <h1 v-else>Else text</h1>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      student: "Student",
      graduated: true,
    };
  },
};
</script>
<style scoped>
h1 {
  color: blue;
}
</style>
