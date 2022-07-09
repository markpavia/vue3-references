<template>
	<div>
		<!-- <Card></Card>
		<Card>Card content</Card>
		<Card>
			<h2>Card content</h2>
		</Card>
		<Card>
			<img src="https://picsum.photos/200" alt="" />
		</Card>

		<Card>
			<template v-slot:header>
				<h3>Header</h3>
			</template>
			<template v-slot:default>
				<img src="https://picsum.photos/200" alt="" />
			</template>
			<template v-slot:footer>
				<button>View Details</button>
			</template>
		</Card> -->

		<!-- CHILD TO PARENT -->
		<NameList>
			<template v-slot:default="slotProps">
				{{ slotProps.firstName }} {{ slotProps.lastName }}
			</template>
		</NameList>

		<NameList>
			<template v-slot:default="slotProps">
				{{ slotProps.lastName }}, {{ slotProps.firstName }}
			</template>
		</NameList>

		<NameList>
			<template v-slot:default="slotProps">
				{{ slotProps.firstName }}
			</template>
		</NameList>
	</div>
</template>

<script>
// import Card from "./components/slots/Card.vue"
import NameList from "./components/slots/NameList.vue"
export default {
	name: "App",
	components: {
		// Card,
		NameList,
	},
	data() {
		return {}
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
