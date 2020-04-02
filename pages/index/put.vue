<template>
	<view>
		<app-bar title="发布"></app-bar>
		<radio :class="radio=='A'?'checked':''" :checked="radio=='A'?true:false" value="A"></radio>
	</view>
</template>

<script>
	import appBar from '../components/appBar.vue'
	export default {
		components:{
			appBar
		},
		data() {
			return {
				radio:'A'
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
