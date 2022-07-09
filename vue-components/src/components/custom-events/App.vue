<template>
	<div>
		<button @click="showPopup = true">Show Popup</button>
		<popup-component v-show="showPopup" @close="closePopup" />
	</div>
</template>

<script>
import PopupComponent from "./components/custom-events/PopupComponent.vue"
export default {
	name: "App",
	components: { PopupComponent },
	data() {
		return {
			showPopup: false,
		}
	},
	methods: {
		closePopup(name) {
			this.showPopup = false
			console.log(`name ${name}`)
		},
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
