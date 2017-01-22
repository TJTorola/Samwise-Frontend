<template>
	<div class="wrapper">
		<input type="text" />
		<span class="label">
			E-Mail
		</span>
		<div class="underline" />
	</div>
</template>

<style scoped>
.wrapper {
	position: relative;
	border: 1px solid black;
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
	top: 17px;
	left: 10px;
	width: 100%;
}

input:focus {
	outline: none;
}

.label {
	position: absolute;
	top: 12px;
	left: 10px;
	transition: all .2ms ease-in-out;
}

input:focus ~ .label {
	top: 5px;
	font-size: 10px;
}
</style>

<script>

</script>