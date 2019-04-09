<template>
  <div id="app">
    <echart-demo></echart-demo>
  </div>
</template>

<script>
import echartDemo from "./components/echarts-demo2";
export default {
  name: "app",
  components: {
    "echart-demo": echartDemo
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
  margin-top: 60px;
}
</style>
