<template>
	<view class="cu-item">
		<navigator class="content">
			<image :src="img" mode="widthFix"></image>
			<!-- <view class="description">
				<view class="text">参考价格:{{price}}</view>
				<view class="text">发布时间:{{time}}</view>
			</view> -->
		</navigator>
		<view class="cu-tag bg-red">{{type}}</view>
	</view>
</template>

<script>
	export default{
		props:['title','img','price','time','type'],
		data(){
			return{
				
			}
		},
		methods:{
			showModal(){
				
			}
		}
	}
</script>

<style scoped>
	.show{
		display: block;
	}
	.cu-item{
		width: 40%;
		margin-left: 5%;
		display: inline-block;
		position: relative;
		height:auto;
		color:#333333;
		padding: 0!important;
	}
	.title{
		padding: 0;
		color: #fff!important;
		line-height: 30px!important;
	}
	.content{
		width: 100%;
		padding: 0!important;
	}
	.cu-item>.content>image{
		display: block;
		width: 100%!important;
		margin: 0!important;
	}
	.cu-tag{
		top:0;
		position: absolute;
	}
	.description{
		width: 80%;
		float: right;
	}
	.description>view{
		height: auto;
		line-height: 30px;
		color:#888;
		padding-left: 10px;
	}
	.icon-group{
		position: absolute;
		bottom: 0;
		right: 10px;
		line-height: 24px;
	}
</style>
