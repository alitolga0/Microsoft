<template>
  <div id="app">
    <div>
      <myNavBar />
    </div>
    <div style="padding-top:40px">
      <mySlider />
    </div>
    <div >
      <myHomePage />
    </div>
    <div >
      <myFooter />
    </div>
  </div>
</template>

<script>
import myNavBar from "./components/NavBar.vue";
import myFooter from "./components/Footer.vue";
import myHomePage from "./components/HomePage.vue";
import mySlider from "./components/Slider.vue";

export default {
  name: "App",
  components: {
    myNavBar,
    myHomePage,
    myFooter,
    mySlider,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
 
}
</style>
