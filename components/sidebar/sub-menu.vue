<template>
	<div>
		<div>{{ menu.catagory }}</div>
		<ul>
			<my-link 
				v-for="link in menu.links"
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