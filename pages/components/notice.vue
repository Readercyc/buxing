<template>
	<view class="cu-item shadow card">
		<view class="cu-list menu-avatar">
			<view class="cu-item">
				<view class="cu-avatar round lg" style="background-image:url(https://ossweb-img.qq.com/images/lol/web201310/skin/big10006.jpg);"></view>
				<view class="content flex-sub">
					<view>{{editor}}</view>
					<view class="text-gray text-sm flex justify-between">
						2019年12月3日
					</view>
				</view>
			</view>
		</view>
		<view class="text-content text-cut">
			{{title}}
		</view>
		<view class="grid flex-sub padding-lr">
			<image :src="img==''?'../../static/noticeDefault.png':img" class="noticeImage"></image>
		</view>
		<view class="text-gray text-sm text-right">
			<text class="cuIcon-attentionfill margin-lr-xs">24211</text> 
			<text class="cuIcon-messagefill margin-lr-xs">2115</text> 
		</view>
	</view>
</template>

<script>
	export default{
		props:['title','time','img','editor']
	}
</script>

<style>
	.card{
		height: auto;
	}
	.noticeImage{
		height:320rpx;
		width: 100%;
	}
</style>
