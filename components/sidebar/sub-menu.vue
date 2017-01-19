<template>
	<div>
		<div class="sub-header">{{ menu.catagory }}</div>
		<ul>
			<li v-for="link in menu.links">
				<icon v-bind:i="link.icon" /> {{ link.name }}
			</li>
		</ul>
	</div>
</template>

<script>
import Icon from '~components/icon.vue';

export default {
	components: {
		Icon
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

.icon {
	fill: #b8c7ce;
	height: 16px;
	position: relative;
	top: 2px;
	margin-right: 8px;
}

ul {
	margin: 0;
	padding: 0;
}

li {
	list-style: none;
	height: 40px;
	line-height: 40px;
	padding: 0 5px 0 15px;
	color: #b8c7ce;
	font-size: 14px;
	border-left: 3px solid transparent;
}

li:hover {
	cursor: pointer;
	color: white;
	background: #1e282c;
	border-left-color: #3c8dbc;
}

li:hover .icon {
	fill: white;
}
</style>