<template>
	<div>
		<h2>Component E</h2>
		<component-f />
	</div>
</template>

<script>
import ComponentF from "./ComponentF.vue"
export default {
	components: { ComponentF },
}
</script>

<style scoped></style>
