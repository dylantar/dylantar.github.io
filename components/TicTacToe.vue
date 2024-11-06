<template>
    <div id="tic-tac-toe">
      <h2>Tic-Tac-Toe Game</h2>
      <div class="board">
        <div
          v-for="(cell, index) in board"
          :key="index"
          class="cell"
          @click="makeMove(index)"
        >
          {{ cell }}
        </div>
      </div>
      <button @click="resetBoard">Reset</button>
    </div>
  </template>
  
  <script>
  import { ref, onMounted } from 'vue';
  
  export default {
    setup() {
      const board = ref(Array(9).fill(null)); // Initial empty board
      const currentPlayer = ref('X'); // Set initial player to X
  
      // Function to make a move
      const makeMove = (index) => {
        if (!board.value[index]) {
          board.value[index] = currentPlayer.value;
          currentPlayer.value = currentPlayer.value === 'X' ? 'O' : 'X';
        }
      };
  
      // Function to reset the board
      const resetBoard = () => {
        board.value = Array(9).fill(null);
        currentPlayer.value = 'X';
      };
  
      // Using onMounted to access DOM after it's rendered
      onMounted(() => {
        console.log('Component is mounted and DOM is ready!');
        const cells = document.querySelectorAll('.cell');
        // Now you can safely interact with the cells if needed
      });
  
      return {
        board,
        currentPlayer,
        makeMove,
        resetBoard
      };
    }
  };
  </script>
  
  <style scoped>
  .board {
    display: grid;
    grid-template-columns: repeat(3, 100px);
    grid-gap: 5px;
  }
  .cell {
    width: 100px;
    height: 100px;
    text-align: center;
    font-size: 2em;
    border: 1px solid #333;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
  }
  button {
    margin-top: 10px;
    padding: 10px;
  }
  </style>
  