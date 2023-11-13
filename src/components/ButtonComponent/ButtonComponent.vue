<template>
	<button class="btn">{{ props.text }}</button>
</template>

<script setup lang="ts">
	import './ButtonComponent.css';

	interface Props {
		text: string;
	}

	const props = withDefaults(defineProps<Props>(), {
		text: 'Start my trial',
	});
</script>
