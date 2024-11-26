<template>
	<view class="home">

		<scroll-view scroll-x class="navScroll">
			<view class="item" v-for="item in 10">國內</view>
		</scroll-view>

		<view class="content">
			<view class="row" v-for="item in 10">
				<!-- <newbox :item="{title:'首頁標題',author:'李四',hits: 700,}"></newbox> -->
				<newbox></newbox>
			</view>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.navScroll {
		height: 100rpx;
		background: #F7F8FA;
		white-space: nowrap;

		.item {
			font-size: 40rpx;
			display: inline-block;
			line-height: 100rpx;
			padding: 0 30rpx;
			color: #333;
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