<template>
	<div>
		<box header="Buttons" sub-header="clicky-doey-things">
			<sw-button icon="user">
				Find User
			</sw-button>

			<sw-button icon="trash" color="danger">
				Delete
			</sw-button>

			<sw-button icon="timesCircle" disabled>
				Disabled Button
			</sw-button>
		</box>

		<box header="Custom Input">
			Plain:
			<sw-input label="E-Mail" />
		</box>

		<box header="Working Buttons">
			<working-button icon="star">
				Become a star
			</working-button>
		</box>

		<box header="Working Icons">
			<working-icon i="user" ref="workingIcon">
		</box>

		<box header="Icons">
			<span v-for="icon in icons" class="icon-wrapper">
			<Icon v-bind:i="icon"/> - {{ icon }}
			</span>
		</box>
	</div>
</template>

<style scoped>
.icon-wrapper {
	display: inline-block;
	width: 300px;
}
</style>

<script>
import Box from '~components/box.vue';
import FA from '~assets/js/fa.js';
import SwButton from '~/components/button.vue';
import WorkingButton from '~/components/working-button.vue';
import WorkingIcon from '~/components/working-icon.vue';
import Icon from '~/components/icon.vue';
import SwInput from '~/components/input.vue';

export default {
	data: () => ({
		icons: Object.keys(FA)
	}),

	components: {
		Box,
		Icon,
		SwButton,
		WorkingIcon,
		WorkingButton,
		SwInput
	}
}
</script>