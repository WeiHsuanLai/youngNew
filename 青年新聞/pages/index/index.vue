<template>
	<view class="home">

		<scroll-view scroll-x class="navScroll">
			<view class="item" :class="index==navIndex?'active':''" v-for="(item,index) in 10" @click="clickNav(index)">
				國內
			</view>
		</scroll-view>

		<view class="content">
			<view class="row" v-for="item in 10">
				<!-- <newbox :item="{title:'首頁標題',author:'李四',hits: 700,}"></newbox> -->
				<newbox @click.native="goDetail"></newbox>
			</view>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				navIndex: 0
			}
		},
		onLoad() {
			// console.log("this.navIndex", this.navIndex);
		},
		methods: {
			clickNav(index) {
				this.navIndex = index
				// console.log("this.navIndex", this.navIndex);
			},
			// 測試
			goDetail() {
				uni.navigateTo({
					url: '/pages/detail/detail',
					success: res => {},
					fail: () => {},
					complete: () => {}
				});
			}
		}
	}
</script>

<style lang="scss">
	.navScroll {
		height: 100rpx;
		background: #F7F8FA;
		white-space: nowrap;
		position: fixed;
		top: var(--window-top);
		left: 0;
		z-index: 10;

		.item {
			font-size: 40rpx;
			display: inline-block;
			line-height: 100rpx;
			padding: 0 30rpx;
			color: #333;

			&.active {
				color: #31c27c;
			}
		}
	}

	.content {
		padding: 30rpx;
		padding-top: 130rpx;

		.row {
			border-bottom: 1px dotted #efefef;
			padding: 20rpx 0;
		}
	}
</style>