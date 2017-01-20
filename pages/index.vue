<template>
	<div>
		<box header="Buttons" sub-header="clicky-doey-things">
			<sw-button icon="user">
				Find User
			</sw-button>

			<sw-button icon="trash" color="danger">
				Delete
			</sw-button>
		</box>
	</div>
</template>

<script>
import Box from '~components/box.vue';
import SwButton from '~/components/button.vue';

export default {
	components: {
		Box,
		SwButton
	}
}
</script>