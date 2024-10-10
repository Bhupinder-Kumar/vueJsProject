<template>
  <div class="about-page">
    <h1>About the Dice Game</h1>

    <section>
      <h2>What is the Dice Game?</h2>
      <p>
        The Dice Game is a simple web-based application built with <strong>Vue.js</strong> that simulates rolling a six-sided die. 
        Users can click the "Roll Dice" button to generate a random number between 1 and 6, mimicking the experience of rolling a physical die. 
        The game also features a fun rolling animation to enhance user experience.
      </p>
    </section>

    <section>
      <h2>Features</h2>
      <ul>
        <li><strong>Random Dice Rolls</strong>: Every time you click "Roll Dice," a random number between 1 and 6 is generated, just like rolling a real die.</li>
        <li><strong>Rolling Animation</strong>: While the dice is rolling, you'll see a temporary message indicating that the dice is rolling, adding a sense of suspense.</li>
        <li><strong>Easy to Use</strong>: A clean and simple interface ensures that anyone can quickly roll the dice with just one click.</li>
      </ul>
    </section>

    <section>
      <h2>Why Was This Project Built?</h2>
      <p>
        This project was built to demonstrate the power of <strong>Vue.js</strong> for building interactive user interfaces. 
        It also serves as a simple introduction to how reactive state management can be used in a fun, interactive game. 
        Additionally, it's a great example for beginners looking to learn the basics of Vue.js, event handling, and random number generation in JavaScript.
      </p>
    </section>

    <section>
      <h2>Technologies Used</h2>
      <ul>
        <li><strong>Vue.js</strong>: A modern JavaScript framework used to build the interactive frontend of the game.</li>
        <li><strong>JavaScript</strong>: Core logic for handling the random dice rolls and game functionality.</li>
        <li><strong>CSS</strong>: Basic styling to create a user-friendly interface and responsive buttons.</li>
      </ul>
    </section>

    <section>
      <h2>How to Use the Dice Game</h2>
      <ol>
        <li>Click on the "Roll Dice" button.</li>
        <li>The game will show "Rolling..." for a brief moment.</li>
        <li>After rolling, the result (a number between 1 and 6) will be displayed on the screen.</li>
        <li>Roll as many times as you like!</li>
      </ol>
    </section>

    <section>
      <h2>Future Features (Ideas)</h2>
      <ul>
        <li><strong>Multiplayer Mode</strong>: Play with friends by taking turns to roll the dice.</li>
        <li><strong>Score Keeping</strong>: Keep track of how many times each player rolls specific numbers.</li>
        <li><strong>Dice Animations</strong>: Add more realistic dice-rolling animations or images.</li>
      </ul>
    </section>
  </div>
</template>

<script setup>
// No additional script logic is needed for this static page
</script>

<style scoped>
.about-page {
  font-family: Arial, sans-serif;
  padding: 20px;
  line-height: 1.6;
  height: calc(100vh - 100px);
  overflow: auto;
}

h1, h2 {
  color: #fff;
}

ul, ol {
  margin-left: 20px;
}

ul {
  list-style-type: disc;
}

ol {
  list-style-type: decimal;
}

p, li {
  margin: 10px 0;
}
</style>
