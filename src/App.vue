<template>
  <div id="app">
    <Scene :left="left" :top="top"/>
    <Keyboard :left="left" :top="top" @move="handleMove"/>
  </div>
</template>

<script>
import Scene from "./components/Scene";
import Keyboard from "./components/Keyboard";

export default {
  name: "App",
  components: {
    Scene,
    Keyboard
  },
  data() {
    return {
      left: 200,
      top: 200
    };
  },

  methods: {
    handleMove(value) {
      switch (value) {
        case "up":
          this.top -= 50;
          break;
        case "down":
          this.top += 50;
          break;
        case "left":
          this.left -= 50;
          break;
        case "right":
          this.left += 50;
          break;
        default:
          break;
      }
    }
  }
};
</script>

<style>
#app {
  height: 600px;
  display: flex;
}
</style>
