<template>
	<div v-bind:class="`button no-select ${ color }`">
		<Icon v-if="icon" v-bind:i="icon" />
		<slot/>
	</div>
</template>

<style scoped>
.button {
	cursor: pointer;
	border: 1px solid black;
	display: inline-block;
	padding: 5px 15px;
	border-radius: 7px;
	margin: 5px;
}

.button:hover {
	color: white;
	fill: white;
}

.default {
	color: #3c8dbc;
	fill: #3c8dbc;
	border-color: #3c8dbc;
}

.default:hover {
	background: #3c8dbc;
}

.danger {
	color: #dd4b39;
	fill: #dd4b39;
	border-color: #dd4b39;
}

.danger:hover {
	background: #dd4b39;
}

.icon {
	height: 16px;
	position: relative;
	top: 1px;
	left: -3px;
}
</style>

<script>
import Icon from '~components/icon'

export default {
	props: {
		icon: String,
		color: {
			type: String,
			default: 'default'
		}
	},

	components: {
		Icon
	}
}
</script>