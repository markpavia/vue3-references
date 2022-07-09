<template>
	<div>
		<h2>Hello {{ fullName }}</h2>
		<button @click="sendEvent">Call Heroes</button>
	</div>
</template>

<script>
import { computed } from 'vue'
export default {
	name: 'PersonGreeting',
	setup(props, context) {
		console.log(context)

		const fullName = computed(() => {
			return `${props.firstName} ${props.lastName}`
		})

		const sendEvent = () => {
			context.emit('callHeroes', fullName.value)
		}

		return {
			fullName,
			sendEvent,
		}
	},
	props: ['firstName', 'lastName'],
	// computed: {
	// 	fullName() {
	// 		return `${this.firstName} ${this.lastName}`
	// 	},
	// },
}
</script>

<style scoped></style>
