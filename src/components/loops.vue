<script setup>
import {rer, computed} from "vue";
const scores = ref([1, 2, 3, 4, 5, 6, 7, 8, 9]);
const highestScore = computed(()=>{
  return  Math.max(highestScore.value);

});
</script>

<template>
  <h1>Scores</h1>
  <ul>
    <li v-for="score in scores" :key="score">
      {{ score }}
    </li>
  </ul>

  <p>Highest score:{{ highestScore }}}}</p>
</template>
