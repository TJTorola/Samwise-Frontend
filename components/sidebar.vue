<template>
	<aside>
		<div class="logo">
			<b>Admin {{ shortName[0] }}</b>
			<span class="thin">{{ shortName.slice(1) }}</span>
		</div>
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
	text-align: center;
	color: white;
	font-size: 20px;
	line-height: 50px;
}
</style>

<script>
import MyMenu from './sidebar/menu.vue';
import config from '../store.config.js';

export default {
	data: () => ({
		shortName: config.shortName
	}),

	components: {
		MyMenu
	}
}
</script>