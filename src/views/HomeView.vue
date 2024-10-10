<script setup>
import { ref } from 'vue'

// Define a reactive counter variable
const counter = ref(0)

// Increment and Decrement methods
const increment = () => {
  counter.value++
}

const decrement = () => {
  counter.value--
}
</script>

<template>
  <main>
    <h1>Counter: {{ counter }}</h1>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
  </main>
</template>
