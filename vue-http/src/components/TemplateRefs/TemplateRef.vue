<template>
	<div>
		<input type="text" ref="inputRef" />
		<PostList ref="postListRef" />
	</div>
</template>

<script>
import PostList from "../GetRequest/PostList.vue"
export default {
	components: { PostList },
	name: "TemplateRef",
	mounted() {
		console.log(this.$refs.postListRef)
		this.$refs.inputRef.focus()
	},
}
</script>

<style scoped></style>
