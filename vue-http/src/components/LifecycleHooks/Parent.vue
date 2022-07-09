<template>
	<div>
		Parent Component
		<button @click="showChild = !showChild">Toggle Child</button>
		<child v-if="showChild" />
	</div>
</template>

<script>
import Child from "./Child.vue"
export default {
	name: "ParentComponent",
	components: { Child },
	data() {
		return {
			showChild: true,
		}
	},
	beforeCreate() {
		console.log("Parent beforeCreate()")
	},
	created() {
		console.log("Parent created()")
	},
	beforeMount() {
		console.log("Parent beforeMount()")
	},
	mounted() {
		console.log("Parent mounted")
	},
	beforeUpdate() {
		console.log("Parent beforeUpdate()")
	},
	update() {
		console.log("Parent updated()")
	},
	beforeUnmount() {
		console.log("Parent beforeUnmount()")
	},
}
</script>

<style scoped></style>
