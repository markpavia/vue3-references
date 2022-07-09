<template>
	<div>
		<h2>Options - {{ o_firstName }}</h2>
		<h2>
			Options - {{ o_firstName }} {{ o_lastName }} a.k.a. {{ o_heroName }}
		</h2>
		<h2>Composition - {{ c_firstName }}</h2>
		<h2>Composition - {{ greet }}</h2>
		<h2>Composition - {{ greetHero }}</h2>
		<h2>Composition - {{ reactiveGreetHero }}</h2>
	</div>
</template>

<script>
import { ref, reactive } from "vue"

export default {
	name: "DataComponent",
	setup() {
		// ref is for primitive types string, number, boolean
		const c_firstName = ref("Clark")
		const c_lastName = ref("Kent")
		const c_heroName = ref("Superman")

		const greet = `Hello ${c_firstName.value}`
		const greetHero = `Hello ${c_firstName.value} ${c_lastName.value} a.k.a ${c_heroName.value}`

		// reactive is for objects
		const state = reactive({
			firstName: "Princess",
			lastName: "Diana",
			heroName: "Wonder Woman",
		})

		const reactiveGreetHero = `Hello ${state.firstName} ${state.lastName} a.k.a ${state.heroName}`

		return {
			c_firstName,
			greet,
			greetHero,
			reactiveGreetHero,
		}
	},
	data() {
		return {
			o_firstName: "Bruce",
			o_lastName: "Wayne",
			o_heroName: "Batman",
		}
	},
}
</script>

<style scoped></style>
