<template>
	<div>
		<div class="sub-header">{{ menu.catagory }}</div>
		<ul>
			<li v-for="link in menu.links">
				{{ link.name }}
			</li>
		</ul>
	</div>
</template>

<script>
export default {
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

li {
	list-style: none;
	padding: 12px 5px 12px 15px;
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
</style>