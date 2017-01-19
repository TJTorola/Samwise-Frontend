<template>
	<aside>
		<div class="logo"></div>
		<my-menu/>
	</aside>
</template>

<style scoped>
aside {
	min-width: 230px;
	height: 100%;
	background: #222d32;
}

.logo {
	height: 50px;
	background: #367fa9;
	width: 100%;
}
</style>

<script>
import MyMenu from './sidebar/menu.vue';

export default {
	components: {
		MyMenu
	}
}
</script>