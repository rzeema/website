<template>
  <div id="app">
    <Sidebar/>
    <Main/>
  </div>
</template>

<script>
import Main from "./components/Main.vue";
import Sidebar from "./components/Sidebar.vue";

export default {
  name: "app",
  components: {
    Main,
    Sidebar
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #cbd2d8;
  margin-top: 60px;
}
</style>
