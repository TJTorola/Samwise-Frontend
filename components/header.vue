<template>
	<header>
		<div class="icon-container">
			<icon i="bars" />
		</div>
	</header>
</template>

<style scoped>
header {
	background: #3c8dbc;
	width: 100%;
	height: 50px;
	display: flex;
}

.title {
	width: 230px;
	height: 100%;
}

.icon-container {
	padding: 16px;
}

.icon-container:hover {
	cursor: pointer;
	background: #357ca5;
}

.icon {
	fill: white;
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