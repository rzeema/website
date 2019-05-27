<template>
  <div class="hello">
    <h1 id="Header">Jack Ruize Ma</h1>
    <p>
      Welcome to my website!
      <br>This will get way better over time.
    </p>
    <h3>Projects</h3>
    <ul>
      <li>
        <a href="https://github.com/rzeema/website" target="_blank" rel="noopener">website</a>
      </li>
      <li>
        <a href="https://github.com/rzeema/RZ64" target="_blank" rel="noopener">Keyboard</a>
      </li>
    </ul>

    <div class="box">
      <h3>Resume</h3>
    </div>

    <h3>Hobbies/Cool Things</h3>
    <ul>
      <li>Mechanical Keyboards</li>
      <li>Video Games</li>
      <li>Can't remember</li>
    </ul>
    <h3>Contact Me</h3>
    <a href="https://www.w3schools.com" target="_blank">Lmaozers</a>

    <h3>Ecosystem</h3>

    <div
      class="textblock"
    >Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
    <div
      class="textblock"
    >Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
    <div
      class="textblock"
    >Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
    <div
      class="textblock"
    >Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
  </div>
</template>

<script>
export default {
  name: "lol",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.box {
  border-radius: 5px;
  padding: 4px;
  background-color: #42b983;
  color: aliceblue;
  width: 100px;
  margin: auto;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}

.textblock {
  margin: auto;
  width: 30%;
  padding: 2%;
}

.hello {
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 0;
}
</style>
