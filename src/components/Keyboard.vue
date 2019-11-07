<template>
  <div id="controls">
    <div id="keyboard">
      <div>
        <button :disabled="top<=-50" name="up" @click="$emit('move',$event.target.name)">&uarr;</button>
      </div>
      <div>
        <button :disabled="left<=50" name="left" @click="$emit('move',$event.target.name)">&larr;</button>
        <button :disabled="top>=450" name="down" @click="$emit('move',$event.target.name)">&darr;</button>
        <button :disabled="left>=350" name="right" @click="$emit('move',$event.target.name)">&rarr;</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Keyboard",
  props: {
    left: Number,
    top: Number
  }
};
</script>

<style scoped>
button {
  cursor: pointer;
}

#controls {
  border: 1px solid green;
  width: 200px;
  display: flex;
}

#keyboard {
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
