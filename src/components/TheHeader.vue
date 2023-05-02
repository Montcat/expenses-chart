<template>
	<div class="header-container">
		<div class="balance-section">
			<span class="balance-header">My Balance</span>
			<span class="balance">&dollar;921.48</span>
		</div>
		<div class="logo">
			<IconBalance />
		</div>
	</div>
</template>

<script setup>
	import IconBalance from "./icons/IconBalance.vue";
</script>

<style lang="scss" scoped>
	.header-container {
		background-color: var(--ec-soft-red);
		border-radius: 1rem;
		padding: 2rem;
		display: flex;
		justify-content: space-between;
		align-items: center;

		.balance-section {
			display: flex;
			flex-direction: column;

			.balance-header {
				font-weight: 400;
				color: var(--ec-cream);
			}
			.balance {
				color: var(--ec-very-pale-orange);
				font-weight: 700;
				font-size: 2rem;
			}
		}
	}

	@media (max-width: 480px) {
		.header-container .balance-section .balance {
			font-size: 1.5rem;
		}
	}
</style>
