<template>
  <Score userScore="0" computerScore="0"/>
</template>

<script>
import Score from './components/Score.vue'

export default {
  name: 'App',
  components: {
    Score
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');
  #app {
    text-align: center;
    font-family: 'Open Sans', sans-serif;
  }
</style>