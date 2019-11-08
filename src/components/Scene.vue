<template>
  <div id="scene">
    <div id="circle" :style="{left: appendPx(left), top: appendPx(top)}"></div>
  </div>
</template>

<script>
export default {
  name: "Scene",
  props: {
    left: Number,
    top: Number
  },
  methods: {
    appendPx(value) {
      return `${value}px`;
    }
  }
};
</script>

<style scoped>
#scene {
  border: 1px solid red;
  width: 400px;
  position: relative;
}

#circle {
  position: absolute;
  box-sizing: border-box;
  width: 100px;
  height: 100px;
  border: 1px solid black;
  border-radius: 50%;
}
</style>
