<template>
  <div id="app">
    <navBar />
    <div class="carousel">
      <button @click="index--" :verify="verifyIndex()" left>&lt;</button>
      <carousel :index="index" />
      <button @click="index++" :verify="verifyIndex()" right>&gt;</button>
    </div>
	<appFooter />
  </div>
</template>

<script>
import navBar from "@/components/navBar";
import carousel from "@/components/carousel";
import appFooter from '@/components/appFooter'

export default {
  name: "app",
  components: {
    navBar,
	carousel,
	appFooter
  },
  data() {
    return {
      index: 0
    };
  },
  methods: {
    verifyIndex() {
      if (this.index > 2) {
        return (this.index = 0);
      } else if (this.index < 0) {
        return (this.index = 2);
      } else {
        return false;
      }
    }
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

.carousel {
  display: grid;
  justify-content: center;
  margin-top: 20px;
  grid-template-columns: 50px 500px 50px;
  grid-gap: 2rem;
}

button[left]{
	background: linear-gradient(to right, #abbaab, #ffffff);
	
}

button[right]{
	background: linear-gradient(to right, #ffffff, #abbaab);
	
}

button {
	font-size: 2rem;
	color: rgba(9, 4, 80, 0.6)
}
</style>
