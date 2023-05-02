<template>
	<div class="graph-container">
		<Bar id="my-chart-id" :options="chartOptions" :data="chartData" />
	</div>
</template>

<script setup>
	import { Bar } from "vue-chartjs";
	import {
		Chart as ChartJS,
		Title,
		Tooltip,
		BarElement,
		CategoryScale,
		LinearScale,
	} from "chart.js";

	ChartJS.register(Title, Tooltip, BarElement, CategoryScale, LinearScale);

	const chartData = {
		labels: ["mon", "tue", "wed", "thu", "fri", "sat", "sun"],
		datasets: [
			{
				data: [17.45, 34.91, 52.36, 31.07, 23.39, 43.38, 25.48],
				backgroundColor: (color) => {
					let colors =
						color.raw > 50 ? "hsl(186, 34%, 60%)" : "hsl(10, 79%, 65%)";
					return colors;
				},
			},
		],
	};
	const chartOptions = {
		responsive: true,
		maintainAspectRatio: false,
	};
</script>

<style lang="scss" scoped>
	.graph-container {
		height: 220px;
		width: 100%;
	}
</style>
