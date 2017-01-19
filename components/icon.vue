<template>
	<svg 
		viewBox="0 0 32 32" 
		xmlns="http://www.w3.org/2000/svg">
		<path v-bind:d="iconPath" />
</template>

<script>
import FA from '~assets/js/fa.js';

export default {
	props: ['i'],

	data: ({ i }) => ({
		iconPath: FA[i]
	})
}
</script>