<template>
	<div class="app-container">
		<main>
			<div class="header-section">
				<TheHeader />
			</div>

			<div class="chart-section">
				<TheChart />
			</div>
		</main>
	</div>
</template>

<script setup>
	import TheHeader from "@/components/TheHeader.vue";
	import TheChart from "./components/TheChart.vue";
</script>

<style lang="scss" scoped>
	main {
		padding: 25vh 25vw;
	}

	@media (max-width: 480px) {
		main {
			padding: 2rem;
		}
	}
</style>
