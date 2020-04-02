<template>
	<view class="cu-item">
		<view class="image">
			<image :src="img"></image>
			<view class="cu-tag tg-black">{{type}}</view>
			<view class="cu-bar bg-shadeBottom">
				<text>{{address}}</text>
			</view>
		</view>
		<view class="cu-list menu-avatar">
			<view class="cu-item">
				<image :src="avatar" class="cu-avatar round lg"></image>
				<view class="content flex-sub">
					<view class="text-grey">{{name}}</view>
					<view class="text-gray text-sm flex justify-between">二十年老店</view>
				</view>
			</view>
			<view class="text-gray text-sm text-right icon-group">
				<text class="cuIcon-attentionfill margin-lr-xs">{{attention}}</text>
				<text class="cuIcon-appreciatefill margin-lr-xs">{{appreciate}}</text>
				<text class="cuIcon-messagefill margin-lr-xs">{{message}}</text>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default{
		props:['img','avatar','name','address','type','attention','appreciate','message']
	}
</script>

<style scope>
	.cu-tag{
		background-color: rgba(255,255,255,0.8)!important;
	}
	.menu-avatar{
		position: relative;
	}
	.cu-item{
		padding:0px!important;
		height:auto!important;
	}
	.cu-list>.cu-item{
		height:150rpx!important;
	}
	.image>image{
		width:100%;
		height:350rpx!important;
	}
	.icon-group{
		position: absolute;
		bottom: 0;
		right: 10px;
		line-height: 24px;
	}
</style>
