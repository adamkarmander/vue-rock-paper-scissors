<template>
  <div id="gameContainer">
    <h1>Please choose one of the following:</h1>
    <button class="myButton">Rock ✊</button>
    <button class="myButton">Paper ✋</button>
    <button class="myButton">Scissors ✌️</button>
  </div>
</template>

<script>
export default {
  name: 'Game',
  props: {

  }
}
</script>

<style scoped>
  #gameContainer {
    margin-top: 70px;
  }

  .myButton {
    margin-left: 1px;
    margin-right: 1px;
    padding-top: 5px;
    padding-bottom: 5px;
    padding-left: 12px;
    padding-right: 12px;
    cursor: pointer;
    font-size: 16px;
    border: none;
    transition-duration: 0.4s;
    background-color: #d9d9d9;
  }

  .myButton:hover {
    padding-top: 9px;
    padding-bottom: 9px;
    padding-left: 16px;
    padding-right: 16px;
    background-color: #42b883;; /* Green */
    color: white;
  }
</style>