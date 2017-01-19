<template>
	<div class="body">
		<sidebar/>
		<main>
			<my-header/>
			<nuxt/>
		</main>
	</div>
</template>

<style scoped>
.body {
	display: flex;
	height: 100%;
}

main {
	width: 100%;
	display: flex;
	flex-direction: column;
}
</style>

<script>
import Sidebar from '~components/sidebar.vue';
import MyHeader from '~components/header.vue';

export default {
	components: {
		Sidebar,
		MyHeader
	}
}
</script>