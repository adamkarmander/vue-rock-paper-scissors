<template>
  <h1 id="title">Vue Rock Paper Scissors</h1>
  <Score :userScore="userScore" :computerScore="computerScore"/>
  <Game @changed="updateScore" />
</template>

<script>
import Score from './components/Score.vue'
import Game from './components/Game.vue'

export default {
  name: 'App',
  components: {
    Score,
    Game
  },
  data() {
    return {
      userScore: 0,
      computerScore: 0
    };
  },
  methods: {
    updateScore(winner) {
      if (winner === 'user') {
        this.userScore += 1;
      }
      else 
      {
        this.computerScore += 1;
      }
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');

  #app {
    text-align: center;
    font-family: 'Open Sans', sans-serif;
    color: black;
  }

  #title {
    font-size: 50px;
    color: #42b883;
  }
</style>