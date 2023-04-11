<template>
  <div id="wrapper">
    <div id="container">
      <div id="square"></div>
      <div id="stretcher"></div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ScrollAnimation',
});
</script>
<style scoped lang="scss">
#wrapper {
  min-height: 100vh;
  height: 600px;
  background: #000;
}
#container {
  background: #fff;
  height: 300px;
  overflow-y: scroll;
  scroll-timeline-name: squareTimeline;
  position: relative;
}
#square {
  background-color: deeppink;
  width: 100px;
  height: 100px;
  margin-top: 100px;
  animation-name: rotateAnimation;
  animation-duration: 3s;
  animation-direction: alternate;
  animation-timeline: squareTimeline;

  position: absolute;
  bottom: 0;
}

@keyframes rotateAnimation {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
</style>
