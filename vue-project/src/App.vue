<template>
  <div>
    <h1 v-if="graduated">{{ student }}</h1>
    <h1 v-else>Else text</h1>
    <button @click="authState" v-if="loggedIn">Log Out</button>
    <button @click="authState" v-else>Login</button>
    <input type="text" placeholder="edit me" v-model="message" />
    <p>{{ message }}</p>
  </div>
  <h2>{{ now }}</h2>
  <ButtonComp>This text can change</ButtonComp>
</template>

<script>
import ButtonComp from "./components/ButtonComp.vue";
export default {
  name: "Home",
  components: {
    ButtonComp,
  },
  data() {
    return {
      loggedIn: true,
      student: "Student",
      graduated: true,
      message: "",
    };
  },
  methods: {
    authState: function () {
      if (this.loggedIn === false) {
        this.loggedIn = true;
      } else {
        this.loggedIn = false;
      }
    },
  },
  computed: {
    now: function () {
      const time = new Date();
      return `${time.getHours()}:${time.getMinutes()}`;
    },
  },
};
</script>
<style scoped>
h1 {
  color: blue;
}
</style>
