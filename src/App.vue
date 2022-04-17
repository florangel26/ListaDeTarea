<template>
  <div id="app">
    <hello-world />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style>
body {
  background: url(assets/fondo.img);
  background-size: cover;
  background-repeat: no-repeat;
}
#app {
  font-family: "Karla", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 80px;
  padding: 40px;
}
</style>
