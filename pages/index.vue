<template>
	<div>
		<Box header="My Box" sub-header="with a subheader" icon="user">
			<h1>Here we are</h1>
			<p>Hello</p>
		</Box>
	</div>
</template>

<script>
import Box from '~components/box/main.vue';

export default {
	components: {
		Box
	}
}
</script>