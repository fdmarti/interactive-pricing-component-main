<template>
	<span class="badge">{{ props.text }}</span>
</template>

<script setup lang="ts">
	import './BadgeComponent.css';

	interface Props {
		text: string;
	}

	const props = withDefaults(defineProps<Props>(), {
		text : 'Default text'
	});

</script>
