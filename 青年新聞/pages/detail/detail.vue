<template>
	<view class="detail">
		<view class="title">文章標題文章標題文章標題文章標題文章標題文章標題文章標題文章標題</view>
		<view class="info">
			<view class="author">編輯:張三</view>
			<view class="time">2024-11-26 17:38:00</view>
		</view>
		<view class="content">
			內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容
		</view>
		<view class="description">
			版權版權版權版權版權版權版權版權版權版權版權版權版權版權版權版權版權
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
	.detail {
		padding: 30rpx;

		.title {
			font-size: 46rpx;
			color: #333;
		}

		.info {
			background: #F6F6F6;
			padding: 10rpx;
			font-size: 22rpx;
			color: #666;
			display: flex;
			justify-content: space-between;
			margin: 30rpx 0;

			.author {}

			.time {}

		}

		.content {}

		.description {}
	}
</style>