<template>
	<sw-button 
		v-bind:icon="currentIcon()"
		v-bind:color="color"
		v-bind:disabled="disabled">
		<slot />
	</sw-button>
</template>

<script>
import SwButton from './button.vue';

export default {
	props: ['icon', 'color', 'disabled'],

	components: {
		SwButton
	},

	methods: {
		currentIcon() {
			return this.icon;
		}
	}
};
</script>
