<script setup>
// Your JavaScript or Vue code goes here
import { ref } from 'vue'

const gameState = ref('X')
</script>

<template>
  <div>
    <h1>Welcome to Tic-Tac-Toe!</h1>
    <p>{{ gameState }}</p>
    <!-- Add your Tic-Tac-Toe game components or logic here -->
  </div>
</template>

<style scoped>
/* Your CSS styles here */
</style>
