<template>
	<view >
		<app-index></app-index>
		<bottom action="index"></bottom>
	</view>
</template>

<script>
	import appIndex from '../components/appIndex.vue' 
	import bottom from '../components/bottom.vue' 
	export default {
		components:{
			appIndex,
			bottom
			
		},
		data() {
			return {
					PageCur: 'basics'
			}
		},
		methods: {
			NavChange: function(e) {
				this.PageCur = e.currentTarget.dataset.cur
			}
		}
	}
</script>

<style scoped>
	
page{
	width: 100%;
	height: 100%;
	
}
</style>
