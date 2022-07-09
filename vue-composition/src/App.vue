<template>
	<div>
		<ClickCounter />
		<HoverCounter />
	</div>
</template>

<script>
import ClickCounter from './components/Reusability/ClickCounter'
import HoverCounter from './components/Reusability/HoverCounter'

export default {
	name: 'App',
	components: {
		ClickCounter,
		HoverCounter,
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
