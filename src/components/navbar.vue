<template>
  <nav>
    <div class="container">
      <div v-on:click="$emit('back')" class="logo">
        <img src="../assets/skirat_logo_vettoriale.svg" alt="" />
        <div class="logoName">Skirat Games</div>
      </div>
      <ul>
        <li v-for="item in items" :key="item">
          <a :href="`#${item.name}`">{{ item.name }}</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "navbar",
  data() {
    return {
      items: [{ name: "New Game" }, { name: "Load Game" }, { name: "Continue" }, { name: "Options" }, { name: "Quit" }],
    };
  },
};
</script>

<style scoped>
nav {
  height: 60px;
  width: 100%;
  position: fixed;
  top: 0;
  background-color: black;
}
nav .container {
  width: 80%;
  height: 100%;
  margin: 0 auto;

  display: flex;
  justify-content: space-between;
  align-items: center;
}
nav .container .logo {
  height: 100%;
  display: flex;
  align-items: center;
}
nav .container .logo img {
  height: 90%;
}
nav .container .logo .logoName {
  display: inline;
  font-size: 25px;
  font-weight: 900;
  color: coral;
  margin-left: 10px;
}
nav .container ul {
  display: flex;
  align-items: center;
  list-style-type: none;
}
nav .container ul li {
  margin-left: 15px;
}
nav .container ul li a {
  text-decoration: none;
  color: coral;
}
</style>
