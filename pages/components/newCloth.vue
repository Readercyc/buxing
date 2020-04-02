<template>
	<view class="cu-item">
		<view class="detail"></view>
		<view class="title bg-red ">{{title}}</view>
		<view class="content">
			<image :src="img"></image>
			<view class="description">
				<view class="text">参考价格:{{price}}</view>
				<view class="text">发布时间:{{time}}</view>
			</view>
		</view>
		<view class="text-gray text-sm text-right icon-group">
			<text class="cuIcon-attentionfill margin-lr-xs">{{attention}}</text>
			<text class="cuIcon-appreciatefill margin-lr-xs">{{appreciate}}</text>
			<text class="cuIcon-messagefill margin-lr-xs">{{message}}</text>
		</view>
	</view>
</template>

<script>
	export default{
		props:['title','img','price','time','attention','appreciate','message'],
		data(){
			return{
				
			}
		}
	}
</script>

<style scoped>
	.cu-item{
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
		padding: 0!important;
	}
	.cu-item>.content>image{
		height: 200rpx!important;
		width: auto;
		margin: 0!important;
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
