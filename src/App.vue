<template>
  <div v-if="mainPage">
    <mainPage />
    <navbar @back="back" />
  </div>
  <div v-if="page1">
    <page1 @play="play" />
  </div>
  <div v-if="page2">
    <sidebar @back="back" @home="home" />
    <page2 />
  </div>
  {{ dio }}
</template>

<script>
//import HelloWorld from "./components/HelloWorld.vue";
import Navbar from "./components/navbar.vue";
import sidebar from "./components/sidebar.vue";
import page1 from "./components/page1.vue";
import page2 from "./components/page2.vue";
import mainPage from "./components/mainPage.vue";

export default {
  name: "App",
  data() {
    return {
      page1: true,
      page2: false,
      mainPage: false,
    };
  },
  components: {
    //HelloWorld,
    Navbar,
    sidebar,
    page1,
    page2,
    mainPage,
  },
  methods: {
    play() {
      this.mainPage = false;
      this.page1 = false;
      this.page2 = true;
      console.log('play');
    },
    back() {
      this.page2 = false;
      this.mainPage = false;
      this.page1 = true;
      console.log('back');
    },
        home() {
      this.page2 = false;
      this.page1 = false;
      this.mainPage = true;
      console.log('main');
    },
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
