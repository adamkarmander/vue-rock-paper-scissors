<template>
  <div id="gameContainer">
    <h1>Please choose one of the following:</h1>
    <button class="myButton" id="rock" @click="displayResults($event)">Rock ✊</button>
    <button class="myButton" id="paper" @click="displayResults($event)">Paper ✋</button>
    <button class="myButton" id="scissors" @click="displayResults($event)">Scissors ✌️</button>
    <div id="results" />
  </div>
</template>

<script>
export default {
  name: 'Game',
  props: {

  },
  methods: {
    generateComputerChoice() {
      const choices = ['rock', 'paper', 'scissors'];
      const randomChoice = choices[Math.floor(Math.random() * choices.length)];
      return randomChoice;
    },
    getWinner(userChoice, computerChoice) {
      switch (userChoice + computerChoice) {
        case 'rockscissors':
        case 'paperrock':
        case 'scissorspaper':
          return 'You win!';
        case 'rockpaper':
        case 'paperscissors':
        case 'scissorsrock':
          return 'Computer wins!';
        default:
          return "It's a draw!";
      }
    },
    displayResults(e) {
      let userChoice = e.target.id;
      let computerChoice = this.generateComputerChoice();

      const userChoiceDisplay = document.createElement('h1');
      userChoiceDisplay.innerHTML = 'Your choice: ' + userChoice;

      const computerChoiceDisplay = document.createElement('h1');
      computerChoiceDisplay.innerHTML = "Computer's choice: " + computerChoice;

      const winnerDisplay = document.createElement('h1');
      winnerDisplay.innerHTML = this.getWinner(userChoice, computerChoice);

      document.getElementById('results').append(userChoiceDisplay, computerChoiceDisplay, winnerDisplay);
    }
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