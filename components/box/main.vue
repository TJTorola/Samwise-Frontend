<template>
	<main>
		<header>
			<Icon i="user" />
			I'm a box header
			<small>
				(With a sub-header)
			</small>
		</header>
		<div class="body">
			Some content...
		</div>
	</main>
</template>

<style scoped>
main {
	color: #444;
	border-top: 4px green solid;
	background: white;
	border-radius: 4px;
}

header {
	padding: 10px;
	padding-top: 6px;
}

.icon {
	height: 15px;
	position: relative;
	top: 1px;
	margin-right: 3px;
}

.body {
	padding: 10px;
}
</style>

<script>
import Icon from '~components/icon.vue';

export default {
	components: {
		Icon
	}
}
</script>