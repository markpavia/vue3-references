<template>
	<div>
		<!-- <GreetComponent name="Bruce" hero-name="Batman" />
		<GreetComponent name="Clark" hero-name="Superman" />
		<GreetComponent name="Diana" hero-name="Wonder Woman" />
		<GreetComponent :name="name" :hero-name="channel" /> -->

		<ArticleComponent
			id="my-article"
			title="Article Title"
			:likes="50"
			:isPublished="true"
		/>
	</div>
</template>

<script>
// import GreetComponent from "./components/component-props/GreetComponent.vue"
import ArticleComponent from "./components/component-props/ArticleComponent.vue"
export default {
	name: "App",
	components: {
		// GreetComponent,
		ArticleComponent,
	},
	data() {
		return {
			name: "Vishwas",
			channel: "Codevolution",
		}
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
