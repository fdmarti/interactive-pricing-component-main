<template>
	<div class="pricing-block">
		<section class="page-views">
			<span class="pageviews">100k pageviews</span>
			<p class="price">
				<span class="amount">${{ valuesForm.rangePrice }}.00</span>
				<span> /month</span>
			</p>
		</section>
		<section class="range">
			<input type="range" min="0" max="50" v-model="valuesForm.rangePrice" />
		</section>
		<section class="billing-block">
			<span>Monthly Billing</span>
			<input
				type="checkbox"
				name="billing"
				v-model="valuesForm.billing"
				id="switch"
			/><label for="switch"></label>
			<span>Yearly Billing</span>
			<BadgeComponent text="25% discount" />
		</section>
		<hr />
		<section class="trial-block">
			<div class="benefits">
				<BenefitsTextComponent
					:text="benefit.text"
					v-for="benefit in benefits"
					:key="benefit.text"
				/>
			</div>
			<ButtonComponent text="Start my trial" />
		</section>
	</div>
</template>

<script setup lang="ts">
	import { reactive } from 'vue';
	import './PricingComponent.css';

	import BadgeComponent from '../BadgeComponent/BadgeComponent.vue';
	import BenefitsTextComponent from '../BenefitTextComponent/BenefitTextComponent.vue';
	import ButtonComponent from '../ButtonComponent/ButtonComponent.vue';

	const valuesForm = reactive({
		rangePrice: 25,
		billing: false,
	});

	const benefits = [
		{ text: 'Unlimited websites' },
		{ text: '100% data ownership' },
		{ text: 'Email reports' },
	];
</script>
