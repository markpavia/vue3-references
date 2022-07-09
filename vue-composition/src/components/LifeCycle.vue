<template>
	<div>
		<h2>Composition API Lifecycle Hooks</h2>
	</div>
</template>

<script>
import {
	onBeforeMount,
	onMounted,
	onBeforeUpdate,
	onUpdated,
	onBeforeUnmount,
	onUnmounted,
} from "vue"

export default {
	name: "LifeCycle",
	setup() {
		onBeforeMount(() => {
			console.log("Lifecycle onBeforeMount()")
		})

		onMounted(() => {
			console.log("Lifecycle onMounted()")
		})

		onBeforeUpdate(() => {
			console.log("Lifecycle onBeforeUpdate()")
		})

		onUpdated(() => {
			console.log("Lifecycle onUpdated()")
		})

		onBeforeUnmount(() => {
			console.log("Lifecycle onBeforeUnmount()")
		})

		onUnmounted(() => {
			console.log("Lifecycle onUnmounted()")
		})
	},
}
</script>

<style scoped></style>
