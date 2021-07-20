<template>
<main>
	<div v-for="item in items" :key="item" :id="item.name">
		{{item.name}}
	</div>
</main>
</template>

<script>
export default {
  name: "mainPage",
  data() {
    return {
      items: [{ name: "New Game" }, { name: "Load Game" }, { name: "Continue" }, { name: "Options" }, { name: "Quit" }],
    };
  },
  components: {
  },
  methods: {
    test() {
      this.page1 = false;
      this.page2 = true;
      console.log('play');
    },

  },
};
</script>

<style scoped>
main{
	margin-top: 60px;
}
div{
	height: 60vh;
	font-weight: 900;
	font-size: 50px;
	color: tomato;
}
</style>
