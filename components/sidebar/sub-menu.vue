<template>
	<div>
		<div class="sub-header">{{ menu.catagory }}</div>
		<ul>
			<my-link v-for="link in menu.links"
				v-bind:link="link"/>
		</ul>
	</div>
</template>

<script>
import MyLink from './link.vue';

export default {
	components: {
		MyLink
	},

	props: ['menu']
}
</script>

<style scoped>
.sub-header {
	background: #1a2226;
	color: #4b646f;
	width: 100%;
	height: 37px;
	padding: 10px 25px 10px 15px;
	font-size: 13px;
}

ul {
	margin: 0;
	padding: 0;
}
</style>