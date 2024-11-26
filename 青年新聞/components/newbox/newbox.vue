<template>
	<view>
		<view class="new">
			<view class="pic">
				<image :src="item.picurl" mode="aspectFill"></image>
			</view>
			<view class="text">
				<text class="title">
					{{item.title}}
				</text>
				<view class="info" v-if="!item.looktime">
					<text>{{item.author}}</text>
					<text>{{item.hits}}瀏覽</text>
				</view>
				<view class="info" v-else>
					<text>瀏覽時間:{{item.looktime}}</text>
				</view>

			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "newbox",
		props: {
			item: {
				type: Object,
				default () {
					return {
						title: "組件內默認的標題",
						author: "張三",
						hits: 668,
						picurl: "/static/images/0.jpg",
						// looktime: "2024-11-26 14:56:00"
					}
				}
			}
		},

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