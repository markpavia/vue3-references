<template>
	<div>
		<h2 v-if="num === 0">The number is zero</h2>
		<h2 v-else-if="num < 0">The number is negative</h2>
		<h2 v-else-if="num > 0">The number is positive</h2>
		<h2 v-else>Not a number</h2>

		<template v-if="display">
			<h2>Vishwas</h2>
			<h2>Codevolution</h2>
			<h2>Vue</h2>
		</template>

		<!-- v-show just add style display none -->
		<h2 v-show="showElement">Using v-show</h2>
		<!-- v-if is not rendered in dom if false -->
		<h2 v-if="showElement">Using v-if</h2>
	</div>
</template>

<script>
export default {
	name: "ConditionalRendering",
	data() {
		return {
			num: "a",
			display: true,
			showElement: false,
		}
	},
}
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
