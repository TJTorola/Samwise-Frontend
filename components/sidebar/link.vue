<template>
	<li>
		{{ link.name }}
	</li>
</template>

<script>
export default {
	props: ['link']
}
</script>

<style scoped>
li {
	list-style: none;
	padding: 12px 5px 12px 15px;
	color: #b8c7ce;
}

li:hover {
	color: white;
}
</style>