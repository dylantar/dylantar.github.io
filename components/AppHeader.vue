<template>
	<header class="bg-blue-500 text-white p-4">
	  <div class="container mx-auto flex justify-between items-center">
		<h1 class="text-xl font-bold">My Website</h1>
		<nav>
		  <ul class="flex space-x-4">
			<li><NuxtLink to="/" class="hover:text-gray-200">Home</NuxtLink></li>
			<li><NuxtLink to="/about" class="hover:text-gray-200">About</NuxtLink></li>
			<li><NuxtLink to="/contact" class="hover:text-gray-200">Contact</NuxtLink></li>
		  </ul>
		</nav>
	  </div>
	</header>
  </template>
  
  <script setup>
  // No need for additional JavaScript or import in this case.
  </script>
  
  <style scoped>
  /* You can add scoped styles here if needed */
  </style>
  