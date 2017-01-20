<template>
	<li v-on:click="go" class="no-select">
		<icon v-bind:i="link.icon" /> {{ link.name }}
	</li>
</template>

<script>
import Icon from '~components/icon.vue';

export default {
	props: ['link'],

	components: {
		Icon
	},

	computed: {
		path() {
			return this.link.name.toLowerCase().replace(/ /g, '-')
		}
	},

	methods: {
		go() {
			this.$router.push(this.path);
		}
	}
}
</script>

<style scoped>
.icon {
	fill: #b8c7ce;
	height: 16px;
	position: relative;
	top: 3px;
	margin-right: 8px;
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