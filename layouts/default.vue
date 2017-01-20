<template>
	<div class="body">
		<sidebar/>
		<main>
			<my-header/>
			<nuxt class="page" />
		</main>
	</div>
</template>

<style scoped>
.body {
	display: flex;
	height: 100%;
}

.page {
	padding: 10px;
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