<template>
  <div id="sidebar">
    <div class="container">
      <div class="logo">
        <img src="../assets/skirat_logo_vettoriale.svg" alt="" />
        <div class="logoName">Skirat Games</div>
      </div>
      <ul>
        <li v-for="item in items" :key="item">
          <a v-on:click="$emit('home')" :href="`#${item.name}`">{{item.name}}</a>
          <hr>
        </li>
        <li v-on:click="$emit('back')">Return</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "sidebar",
  data() {
    return {
      dio: "Caro",
      items: [{ name: "New Game" }, { name: "Load Game" }, { name: "Continue" }, { name: "Options" }, { name: "Quit" }],
    };
  },
};
</script>

<style scoped>
#sidebar {
  height: 100vh;
  width: 40%;
  position: fixed;
  top: 0;
  background-color: black;
}
#sidebar .container {
  width: 80%;
  height: 100%;
  margin: 0 auto;

  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
#sidebar .container .logo {
  display: flex;
  align-items: center;
}
#sidebar .container .logo img {
  height: 150px;
}
#sidebar .container .logo .logoName {
  display: inline;
  font-size: 60px;
  font-weight: 900;
  color: coral;
  margin-left: 10px;
}
#sidebar .container ul {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  list-style-type: none;
}
#sidebar .container ul li {
  width: 100%;
  margin-top: 7px;
}
#sidebar .container ul li a {
  margin-bottom: 14px;

  text-decoration: none;
  color: coral;
  font-size: 30px;
}
#sidebar .container ul li hr{
  border: 1px solid white;
  width: 60%;
  margin: 0 auto;
}
</style>
