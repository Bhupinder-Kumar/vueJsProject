<script setup>
import { reactive } from 'vue'

// Reactive state to hold the current dice value and game status
const state = reactive({
  diceValue: null, // Initially, no dice value
  rolling: false, // To show a loading state while the dice is rolling
})

// Function to roll the dice
const rollDice = () => {
  if (state.rolling) return

  // Set rolling state to true to simulate dice roll animation
  state.rolling = true

  // Simulate a delay to mimic the rolling effect
  setTimeout(() => {
    // Generate a random number between 1 and 6
    state.diceValue = Math.floor(Math.random() * 6) + 1
    state.rolling = false
  }, 1000) // Dice "rolls" for 1 second
}
</script>

<template>
  <div class="dice-game">
    <h1>Dice Game</h1>

    <!-- Display dice value or a message while rolling -->
    <div class="dice-value">
      <template v-if="state.rolling">
        <p>Rolling...</p>
      </template>
      <template v-else>
        <p v-if="state.diceValue">You rolled: {{ state.diceValue }}</p>
        <p v-else>Click "Roll Dice" to start!</p>
      </template>
    </div>

    <!-- Roll Dice button -->
    <button @click="rollDice" :disabled="state.rolling">Roll Dice</button>
  </div>
</template>

<style scoped>
.dice-game {
  text-align: center;
  font-family: Arial, sans-serif;
}

.dice-value {
  margin: 20px 0;
  font-size: 24px;
}

button {
  padding: 10px 20px;
  font-size: 18px;
  cursor: pointer;
  border-radius: 5px;
  background-color: #007bff;
  color: white;
  border: none;
}

button:disabled {
  background-color: gray;
  cursor: not-allowed;
}
</style>
