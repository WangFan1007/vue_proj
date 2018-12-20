<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <!-- <Test/> -->
    <Guide/>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import Test from "./components/Test";
import Guide from "./components/Guide";

export default {
  name: "app",
  components: {
    // HelloWorld,
    // Test
    Guide
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0;
  background-color: #eee;
}
</style>
