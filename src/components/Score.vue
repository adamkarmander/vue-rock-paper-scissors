<template>
  <div>
    <h1>Score: {{userScore}}-{{computerScore}} (You-Computer)</h1>
  </div>
</template>

<script>
export default {
  name: 'Score',
  props: {
    userScore: {
      type: Number,
      required: true
    },
    computerScore: {
      type: Number,
      required: true
    }
  }
}
</script>
