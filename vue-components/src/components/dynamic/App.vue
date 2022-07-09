<template>
	<div>
		<button @click="activeTab = 'TabA'">Tab A</button>
		<button @click="activeTab = 'TabB'">Tab B</button>
		<button @click="activeTab = 'TabC'">Tab C</button>

		<component :is="activeTab" />

		<keep-alive>
			<component :is="activeTab" />
		</keep-alive>

		<!-- <TabA v-if="activeTab === 'TabA'" />
		<TabB v-if="activeTab === 'TabB'" />
		<TabC v-if="activeTab === 'TabC'" /> -->
	</div>
</template>

<script>
import TabA from "./components/dynamic-components/TabA.vue"
import TabB from "./components/dynamic-components/TabB.vue"
import TabC from "./components/dynamic-components/TabC.vue"
export default {
	name: "App",
	components: { TabA, TabB, TabC },
	data() {
		return {
			activeTab: "TabA",
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
