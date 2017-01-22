<template>
	<div class="wrapper">
		<input type="text" v-model="value" />
		<span class="label" v-bind:class="{ filled }">
			E-Mail
		</span>
	</div>
</template>

<style scoped>
.wrapper {
	position: relative;
	border: 1px solid #444;
	border-radius: 5px;
	padding: 3px;
	height: 45px;
	cursor: text;
}

input {
	border: none;
	background: transparent;
	position: absolute;
	font-size: 15px;
	top: 0;
	left: 0;
	padding-left: 10px;
	padding-top: 10px;
	width: 100%;
	height: 100%;
}

input:focus {
	outline: none;
}

.label {
	position: absolute;
	top: 12px;
	left: 10px;
	transition: 0.2s ease all;
}

input:focus ~ .label, .label.filled {
	top: 5px;
	font-size: 10px;
}
</style>

<script>
export default {
	data: () => ({
		value: ''
	}),

	computed: {
		filled() {
			return this.value !== '';
		}
	}
}
</script>