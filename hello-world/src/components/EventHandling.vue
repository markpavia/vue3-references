<template>
	<div>
		<h2>{{ name }}</h2>
		<div>
			<button @click="changeName">Change Name</button>
			<button @mouseover="changeName, increment(1, $event)">
				Change Name Mouseover
			</button>
		</div>

		<h2>{{ count }}</h2>
		<div>
			<button @click="increment(1, $event)">Increment</button>
			<button @click="increment(5)">Increment 5</button>
			<button @click="decrement(1)">Decrement</button>
			<button @click="decrement(5)">Decrement 5</button>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			name: "Vishwas",
			count: 0,
		}
	},
	methods: {
		changeName(event) {
			this.name = "Batman"
			console.log(event)
		},
		increment(num, event) {
			this.count += num
			console.log(event)
		},
		decrement(num) {
			this.count -= num
		},
	},
}
</script>

<style lang="scss" scoped></style>
