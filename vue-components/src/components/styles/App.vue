<template>
	<div>
		<h4>App component text</h4>
		<ChildStyles>
			<h4>Child component text</h4>
		</ChildStyles>
	</div>
</template>

<script>
import ChildStyles from "./components/styles/ChildStyles.vue"
export default {
	name: "App",
	components: { ChildStyles },
	data() {
		return {}
	},
}
</script>

<style scoped>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}

h4 {
	color: orange;
}
</style>
