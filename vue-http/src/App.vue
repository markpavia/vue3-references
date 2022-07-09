<template>
	<div>
		<click-counter />
		<hover-counter />
	</div>
</template>

<script>
import ClickCounter from "./components/MixinsReusability/ClickCounter.vue"
import HoverCounter from "./components/MixinsReusability/HoverCounter.vue"
export default {
	name: "App",
	components: { ClickCounter, HoverCounter },
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
