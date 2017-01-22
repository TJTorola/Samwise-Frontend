<template>
	<div class="menu">
		<sub-menu 
			v-for="subMenu in subMenus"
			v-bind:menu="subMenu" />
	</div>
</template>

<style scoped>
.menu {
	flex-grow: 1;
}
</style>

<script>
import SubMenu from './sub-menu.vue';
import SUB_MENUS from '~assets/js/config/menu.js';

export default {
	components: {
		SubMenu
	},

	data: () => ({
		subMenus: SUB_MENUS
	})
}
</script>