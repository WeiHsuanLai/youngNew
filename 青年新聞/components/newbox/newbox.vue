<template>
	<view>
		<view class="new">
			<view class="pic">
				<image src="/static/images/0.jpg" mode="aspectFill"></image>
			</view>
			<view class="text">
				<text class="title">默認新聞標題默認新聞標題默認新聞標題默認新聞標題默認新聞標題默認新聞標題默認新聞標題默認新聞標題默認新聞標題</text>
				<view class="info">
					<text>作者名稱</text>
					<text>999瀏覽</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "newbox",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.new {
		display: flex;

		.pic {
			width: 230rpx;
			height: 160rpx;

			image {
				width: 100%;
				height: 100%;
			}
		}

		.text {
			flex: 1;
			padding-left: 20rpx;
			display: flex;
			flex-direction: column;
			justify-content: space-between;

			.title {
				font-size: 36rpx;
				color: #333;
				display: -webkit-box;
				/* 使用 WebKit 的彈性盒子模型 */
				-webkit-box-orient: vertical;
				/* 設置主軸為垂直方向 */
				-webkit-line-clamp: 2;
				/* 限制顯示的行數 */
				overflow: hidden;
				/* 隱藏超出容器的文字 */
				text-overflow: ellipsis;
				/* 添加省略號 */
			}

			.info {
				font-size: 26rpx;
				color: #999;

				text {
					padding-right: 30rpx;
				}
			}
		}
	}
</style>