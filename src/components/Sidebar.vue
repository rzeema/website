<template>
  <div class="sidebar">
    <a href="#Header">
      <img src="https://image.flaticon.com/icons/svg/25/25694.svg" alt="Smiley face" height="42" width="42">
    </a>
    <a href="#">Projects</a>
    <a href="#">Resume</a>
    <a href="#">Skills</a>
    <a href="#">Contact</a>
    <a href="#">Hobbies</a>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  props: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sidebar {
  position: fixed;
  width: 90px;
  height: 100%;
  background-color: #555;
  top: 0%;
  left: 0%;
  z-index: 1;
}
.sidebar a {
  display: block;
  text-align: center;
  padding: 16px;
  transition: 0.3s;
  color: white;
}
.sidebar a:hover {
  background-color: #000;
}
</style>
