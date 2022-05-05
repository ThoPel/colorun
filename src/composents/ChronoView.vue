<template>
  <div>
    <p class="time-text-wrapper">
      <span class="time-text">{{ stopwatch.minutes }}</span
      >:<span class="time-text">{{ stopwatch.seconds }}</span>
    </p>
    <button @click="stopwatch.start()">Start</button>
    <button @click="stopwatch.pause()">Pause</button>
    <button @click="stopwatch.reset()">Reset</button>
  </div>
</template>


<script setup lang="ts">
import { useStopwatch } from "vue-timer-hook";

const autoStart = true;
const stopwatch = useStopwatch(autoStart);
</script>

<style scoped>
.time-text-wrapper,
.time-text {
  font-size: 8.696vw;
  color: #000;
}
</style>