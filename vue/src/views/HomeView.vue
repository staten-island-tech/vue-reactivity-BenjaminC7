<template>
  <h1 v-if="selected === 'A'">A</h1>
  <h1 v-else-if="selected === 'B'">B</h1>
  <h1 v-else-if="selected === 'C'">C</h1>
  <h1 v-else>Choose A, B, or C</h1>
  <select v-model="selected">
    <option value="A">A</option>
    <option value="B">B</option>
    <option value="C">C</option>
  </select>
</template>
<script>
export default {
  data() {
    return {
      graduated: false,
      student: "Yifan",
      animals: ["pig", "cow", "ostrich", "Leon"],
      text: "",
      selected: "",
    };
  },
};
</script>
