<template>
	<view class="cu-bar search bg-white">
		<view class="search-form round">
			<text class="cuIcon-search"></text>
			<input @focus="InputFocus" @blur="InputBlur" :adjust-position="false" type="text" placeholder="文字搜索" confirm-type="search"></input>
		</view>
		<view class="action">
			<button class="cu-btn bg-gradual-red  round">搜索</button>
			<button class="cu-btn bg-gradual-red  round">识别</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				InputBottom: 0
			};
		},
		methods: {
			InputFocus(e) {
				this.InputBottom = e.detail.height
			},
			InputBlur(e) {
				this.InputBottom = 0
			}
		}
	}
</script>

<style>
	.cu-btn{
		margin-right: 5px;
	}
	.search{
		position: fixed;
		z-index: 999;
		top: 45px;
		width: 100%;
	}
</style>
