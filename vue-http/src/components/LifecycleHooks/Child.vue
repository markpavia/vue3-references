<template>
	<div>Child component</div>
</template>

<script>
export default {
	name: "ChildComponent",
	beforeCreate() {
		console.log("Child beforeCreate()")
	},
	created() {
		console.log("Child created()")
	},
	beforeMount() {
		console.log("Child beforeMount()")
	},
	mounted() {
		console.log("Child mounted")
	},
	beforeUpdate() {
		console.log("Child beforeUpdate()")
	},
	update() {
		console.log("Child updated()")
	},
	beforeUnmount() {
		console.log("Child beforeUnmount()")
	},
}
</script>

<style scoped></style>
