<template>
	<div>
		<my-header/>
		<sidebar/>
		<nuxt/>
	</div>
</template>

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