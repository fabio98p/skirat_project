<template>
  <div v-if="mainPage">
    <HelloWorld  msg="Welcome to Your Vue.js App" />
    <navbar />
  </div>
    <div v-if="page1">
    <page1 />
  </div>
  <div v-if="page2">
    <sidebar />
    <page2 />
  </div>
  {{ dio }}
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Navbar from "./components/navbar.vue";
import sidebar from "./components/sidebar.vue";
import page1 from "./components/page1.vue";
import page2 from "./components/page2.vue";

export default {
  name: "App",
  data() {
    return {
      page1: false,
      page2: false,
      mainPage: true,
    };
  },
  components: {
    HelloWorld,
    Navbar,
    sidebar,
    page1,
    page2,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  border: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
