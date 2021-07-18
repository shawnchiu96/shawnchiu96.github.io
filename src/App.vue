<template>
  <div class="light-mode" id="app">
    <page-basic>
      <template v-slot:page-body>
        <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
        <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
        <image-page-view
          title="页面暂不可用"
          content="迁移准备中，请稍后再试"
        ></image-page-view>
      </template>
    </page-basic>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import PageBasic from "./components/page-basic/src/page-basic.vue";
import ImagePageView from './components/image-page-view/src/image-page-view.vue';

export default {
  name: "App",
  components: {
    // HelloWorld,
    PageBasic,
    ImagePageView
  },
};
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}

.boxxx {
  width: 300px;
  height: 100px;
  background-color: greenyellow;
}
</style>
