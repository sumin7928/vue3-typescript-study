<template>
  <h1>Timer Example</h1>
  <div id="counter">
    Counter: {{ counter }}
  </div>
  <button v-on:click="stopTimer">Stop Timer</button>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class Rendering extends Vue {
  counter = 0;
  timerNo = 0;

  data() {
    return {
      counter: 0
    };
  }
  mounted() {
    this.timerNo = setInterval(() => {
      this.counter++;
    }, 1000);
  }

  stopTimer() {
    clearInterval(this.timerNo);
  }
}
</script>

<style>
</style>