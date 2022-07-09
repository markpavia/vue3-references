<template>
	<div>
		<h2>Volume Tracker (0-20)</h2>
		<h3>Current Volume {{ volume }}</h3>
		<div>
			<button @click="volume += 2">Increase</button>
			<button @click="volume -= 2">Decrease</button>
		</div>

		<input type="text" v-model="movie" />
		<input type="text" v-model="movieInfo.title" />
		<input type="text" v-model="movieInfo.actor" />

		<div>
			<button @click="movieList.push('Wonder Woman')">Add Movie</button>

			<!-- Concat returns a new array and not edit the existing array. So we can remove deep: true -->
			<button @click="movieList = movieList.concat('Wonder Woman')">
				Add Movie 2
			</button>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			volume: 0,
			movie: "Batman",
			movieInfo: {
				title: "",
				actor: "",
			},
			movieList: ["Batman", "Superman"],
		}
	},
	methods: {},
	computed: {},
	watch: {
		volume(newValue, oldValue) {
			if (newValue === 16 && newValue > oldValue) {
				alert(
					"Listening to a high valume for a long time may damage your hearing"
				)
			}
		},
		// NORMAL WATCHER
		// movie(newValue) {
		// 	console.log(`Calling API with movie name = ${newValue}`)
		// },

		// RUN WATCHER ON PAGE LOAD
		movie: {
			handler(newValue) {
				console.log(`Calling API with movie name = ${newValue}`)
			},
			immediate: true,
		},
		// WATCH NESTED PROPERTIES
		movieInfo: {
			handler(newValue) {
				console.log(
					`Calling API with movie ${newValue.title} and actor ${newValue.actor}`
				)
			},
			deep: true,
		},
		movieList: {
			handler(newValue) {
				console.log(`Updated list ${newValue}`)
			},
			deep: true,
		},
	},
}
</script>

<style lang="scss" scoped></style>
