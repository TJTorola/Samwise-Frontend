<template>
	<header>
		<div class="container">
			<icon i="bars" />
		</div>

		<div class="spacer" />

		<div class="container">
			<icon i="shoppingCart" />
		</div>

		<div class="container thin">
			Tyler Torola
		</div>
	</header>
</template>

<style scoped>
header {
	color: white;
	fill: white;
	background: #3c8dbc;
	width: 100%;
	height: 50px;
	display: flex;
}

.title {
	width: 230px;
	height: 100%;
}

.spacer {
	flex-grow: 1;
}

.container {
	padding: 16px;
}

.container:hover {
	cursor: pointer;
	background: #357ca5;
}

.icon {
	height: 16px;
}
</style>

<script>
import Icon from "~components/icon.vue";

export default {
	components: {
		Icon
	}
};
</script>