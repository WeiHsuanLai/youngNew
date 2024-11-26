<template>
	<view class="user">
		<view class="top">
			<image src="/static/images/clock.png" mode="aspectFill"></image>
			<text>瀏覽歷史</text>
		</view>

		<view class="content">
			<view class="row" v-for="item in 10">
				<!-- <newbox :item="{title:'user的標題',looktime:'2024-11-27 17:08:00',}"></newbox> -->
				<newbox></newbox>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.user {
		.top {
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-items: center;
			background: #f8f8f8;
			color: #555;
			font-size: 38rpx;
			padding: 20rpx;

			image {
				width: 200rpx;
				height: 200rpx;
			}
		}
	}

	.content {
		padding: 30rpx;

		.row {
			border-bottom: 1px dotted #efefef;
			padding: 20rpx 0;
		}
	}
</style>