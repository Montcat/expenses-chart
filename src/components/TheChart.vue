<template>
	<div class="chart-container">
		<div class="chart-header">
			<span>Spending - Last 7 days</span>
		</div>

		<div class="chart-data-container">
			<TheChartGraphVue />
		</div>

		<div class="total">
			<div class="left">
				<span class="topic">Total this month</span>
				<span class="results">&dollar;478.33</span>
			</div>
			<div class="right">
				<span class="percentage-gained">&plus;2.4%</span>
				<span class="last-update">from last month</span>
			</div>
		</div>
	</div>
</template>

<script setup>
	import TheChartGraphVue from "./TheChartGraph.vue";
</script>

<style lang="scss" scoped>
	.chart-container {
		background-color: var(--ec-very-pale-orange);
		margin-top: 2rem;
		padding: 2rem;
		border-radius: 1rem;

		// chart header section
		.chart-header {
			margin-bottom: 1rem;

			span {
				font-size: 2rem;
				font-weight: 700;
				color: var(--ec-dark-brown);
			}
		}

		// Total section
		.total {
			display: flex;
			justify-content: space-between;
			margin-top: 1rem;

			.left {
				display: flex;
				flex-direction: column;

				.topic {
					opacity: 0.5;
					font-size: 1.2rem;
				}

				.results {
					font-size: 3rem;
					font-weight: 700;
					color: var(--ec-dark-brown);
				}
			}

			.right {
				display: flex;
				flex-direction: column;
				align-self: end;

				.percentage-gained {
					font-weight: 700;
					font-size: 1.2rem;
					align-self: end;
					color: var(--ec-dark-brown);
				}

				.last-update {
					font-size: 1.2rem;
					opacity: 0.5;
				}
			}
		}
	}

	@media (max-width: 480px) {
		.chart-container {
			.chart-header > span {
				font-size: 1.5rem;
			}

			.total {
				.left {
					.topic {
						font-size: 1rem;
					}

					.results {
						font-size: 2rem;
					}
				}
			}

			.right {
				.percentage-gained {
					font-size: 1rem;
				}

				.last-update {
					font-size: 1rem;
				}
			}
		}
	}
</style>
