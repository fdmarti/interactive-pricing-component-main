<template>
	<span class="benefit">{{ props.text }}</span>
</template>

<script setup lang="ts">
	import './BenefitTextComponent.css';

	interface Props {
		text: string;
	}

	const props = withDefaults(defineProps<Props>(), {
		text: 'Default benefits',
	});
</script>
