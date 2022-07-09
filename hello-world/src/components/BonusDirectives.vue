<template>
	<div>
		<h2 v-once>{{ name }}</h2>
		<button @click="name = 'Batman'">Change name</button>

		<!-- element will not be added on compilation -->
		<h2 v-pre>{{ name }}</h2>
	</div>
</template>

<script>
export default {
	data() {
		return {
			name: "Vishwas",
		}
	},
}
</script>

<style lang="scss" scoped></style>
