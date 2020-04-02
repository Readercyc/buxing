<template>
	<view class="cu-bar tabbar bg-white fixBottom">
		<view class="action" :class="action=='me'?'text-gray':'text-red'">
			<navigator url="/" class="cuIcon-homefill"></navigator> 首页
		</view>
		<view class="action text-gray add-action">
			<navigator url="./put" class="cu-btn cuIcon-add bg-red shadow"></navigator>
			发布
		</view>
		<view class="action" :class="action=='me'?'text-red':'text-gray'">
			<navigator url="./me" class="cuIcon-my">
			</navigator>
			我的
		</view>
	</view>
</template>

<script>
	export default{
		props:['action']
	}
</script>

<style>
.fixBottom{
		position: fixed;
		bottom: 0px;
		width: 100%;
}
</style>
