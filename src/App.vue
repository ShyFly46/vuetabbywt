<template>
	<div>
		Likes: {{ likes }}
	</div>
	<button @click="addLike">Like!</button>
</template>

<script>
export default {
	data() {
		return {
			likes: 4,
			}
	},	

	methods: {
		addLike(){
			this.likes++;
		}
	}
}
</script>

<style>
</style>

