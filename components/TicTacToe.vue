<template>
    <div>
      <h2 class="text-center text-xl">Tic Tac Toe</h2>
      <div id="turn" class="my-4 text-center">X's Turn</div>
      <table class="mx-auto border-collapse">
        <tbody>
          <tr>
            <td class="game-cell"></td>
            <td class="game-cell"></td>
            <td class="game-cell"></td>
          </tr>
          <tr>
            <td class="game-cell"></td>
            <td class="game-cell"></td>
            <td class="game-cell"></td>
          </tr>
          <tr>
            <td class="game-cell"></td>
            <td class="game-cell"></td>
            <td class="game-cell"></td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const turn = ref('X')
  
  const changeTurn = () => {
    turn.value = turn.value === 'X' ? 'O' : 'X'
  }
  
  const handleClick = (event) => {
    const cell = event.target
    if (!cell.textContent) {
      cell.textContent = turn.value
      changeTurn()
    }
  }
  
  const cells = ref([])
  
  const initGame = () => {
    const gameCells = document.querySelectorAll('.game-cell')
    cells.value = Array.from(gameCells)
    cells.value.forEach((cell) => {
      cell.addEventListener('click', handleClick)
    })
  }
  
  initGame()
  </script>
  
  <style scoped>
  .game-cell {
    width: 60px;
    height: 60px;
    border: 1px solid black;
    text-align: center;
    font-size: 2rem;
    cursor: pointer;
  }
  </style>
  