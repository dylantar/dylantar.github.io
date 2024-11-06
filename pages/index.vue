<template>
	<PrimePanel header="Welcome to My Personal Website" class="my-6">
	  <p>Welcome to my personal website! Here you'll find my projects, resume, and a fun Tic Tac Toe game.</p>
	  <PrimeButton label="Go to Tic Tac Toe" icon="pi pi-game" @click="goToTicTacToe" />
	</PrimePanel>
  </template>
  
  <script setup>
  const goToTicTacToe = () => {
	// Navigates to the Tic Tac Toe page
	useRouter().push('/games')
  }
  </script>
  
  <style scoped>
  /* Add any additional styles if needed */
  </style>
  