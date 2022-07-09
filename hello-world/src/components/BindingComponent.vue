<template>
	<div>
		<!-- BINDING TEXT -->
		<div>{{ greet }} {{ name }}</div>
		<div v-text="channel"></div>
		<!-- Below will return error "v-text will override element children."-->
		<!-- <div v-text="name">Hello</div>  -->

		<!-- BINDING HTML -->
		<div v-html="channel"></div>
		<div v-html="hack"></div>
		<h2 :id="headingId">Heading</h2>
		<button :disabled="isDisabled">Bind</button>

		<!-- BINDING CLASSES -->
		<h2 class="underline">Underlined Text</h2>
		<h2 class="underline" :class="status">Status</h2>
		<h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
		<h2 :class="isSoldOut ? 'sold-out' : 'new'">Soldout? movie</h2>
		<h2 :class="['new', 'promoted']">Newly promoted movie</h2>
		<h2 :class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">
			Array conditional movie
		</h2>
		<h2
			:class="{
				promoted: isPromoted,
				new: !isSoldOut,
				'sold-out': isSoldOut,
			}"
		>
			Object conditional movie
		</h2>

		<!-- BINDING INLINE STYLES -->
		<h2
			:style="{
				color: highlightColor,
				fontSize: headerSize + 'px',
				padding: '20px',
			}"
		>
			Inline Style
		</h2>
		<h2 :style="headerStyleObject">Style Object</h2>
		<div :style="[baseStyleObject, successStyleObject]">Success Style</div>
		<div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
	</div>
</template>

<script>
export default {
	name: "BindingComponent",
	data() {
		return {
			// BINDING TEXT
			greet: "Hello",
			name: "Batman",

			// BINDING HTML
			channel: "<b>Codevolution</b>",
			hack: `<a href="#" onclick="alert('You have been hacked!')">Win a prize!</a>`,
			headingId: "heading",
			isDisabled: true,

			// BINDING CLASSES
			status: "success",
			isPromoted: true,
			isSoldOut: true,

			// BINDING INLINE STYLES
			highlightColor: "orange",
			headerSize: 50,
			headerStyleObject: {
				color: "orange",
				fontSize: "50px",
				padding: "20px",
			},
			baseStyleObject: {
				fontSize: "50px",
				padding: "10px",
			},
			successStyleObject: {
				color: "green",
				backgroundColor: "lightgreen",
				border: "1px solid green",
				padding: "20px",
			},
			dangerStyleObject: {
				color: "darkred",
				backgroundColor: "red",
				border: "1px solid darkred",
			},
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
.underline {
	text-decoration: underline;
}

.promoted {
	font-style: italic;
}

.new {
	color: olivedrab;
}

.sold-out {
	color: red;
}
</style>
