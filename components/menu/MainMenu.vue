<script setup>
// Libraries
import { ref } from 'vue'

// Dark mode state
const checked = ref(false);

// Menu items with added links
const items = ref([
	{
		label: 'Home',
		icon: 'pi pi-home',
		route: '/'
	},
	{
		label: 'About',
		icon: 'pi pi-info',
		route: '/about'
	},
	{
		label: 'Resume',
		icon: 'pi pi-file',
		route: '/resume'
	},
	{
		label: 'Games',
		icon: 'pi pi-game',
		route: '/games'
	}
]);

// Toggle dark mode
function toggleDarkMode() {
	document.documentElement.classList.toggle('p-dark');
}

</script>

<template>
	<PrimeMenubar :model="items">
		<template #start>
			<!-- You can add a logo or any other start section here -->
		</template>

		<template #item="{ item }">
			<NuxtLink :to="item.route" class="flex items-center space-x-2">
				<span v-if="item.icon" :class="item.icon" />
				<span>{{ item.label }}</span>
			</NuxtLink>
		</template>

		<template #end>
			<PrimeToggleButton v-model="checked" @change="toggleDarkMode"
				onIcon="pi pi-moon" onLabel="Toggle" 
				offIcon="pi pi-sun" offLabel="Toggle" 
				class="w-36" aria-label="Toggle Dark Mode" v-tooltip.bottom="'Toggle Dark Mode'" />
		</template>
	</PrimeMenubar>
</template>

<style scoped>
/* Optional styling for the menu */
</style>
