<template>
	<view class="masterNode">
		<scroll-view scroll-y="true" style="height: 100%;">
			<view class="nodeBox">
				<view class="node-item" @click="onPageJump('/pages/index/nodeDetail')">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
				<view class="node-item">
					<view class="name">
						MN-6884
					</view>
					<view class="total">
						123456.654
					</view>
					<view class="today">
						今日+1234.321
					</view>
				</view>
			</view>
		</scroll-view>
		<view class="bottomBtn">
			<view class="addNode" @click="onPageJump('/pages/index/masterNodeCreate')">
				添加节点
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {}
		},
		onLoad() {

		},
		methods: {
			onPageJump(url) {
				uni.navigateTo({
					url: url
				});
			}
		}
	}
</script>

<style lang="less">
	.masterNode {
		height: 100%;
	}

	.nodeBox {
		// height: 100%;
		width: 100%;
		display: flex;
		flex-wrap: wrap;
		padding: 50rpx 0;

		.node-item {
			width: 334rpx;
			height: 404rpx;
			color: #FFFFFF;
			font-size: 24rpx;
			padding: 34rpx;

			.name {
				font-size: 38rpx;
			}

			.total {
				margin: 15rpx 0 150rpx;
			}

			.today {}
		}

		.node-item:nth-child(4n+1) {
			margin: 0 38rpx 0 22rpx;
			background: url(../../static/node_bg_one.png) no-repeat;
			background-size: 100% 100%;
		}

		.node-item:nth-child(4n+2) {
			background: url(../../static/node_bg_two.png) no-repeat;
			background-size: 100% 100%;
		}

		.node-item:nth-child(4n+3) {
			margin: 0 38rpx 0 22rpx;
			background: url(../../static/node_bg_three.png) no-repeat;
			background-size: 100% 100%;
		}

		.node-item:nth-child(4n+4) {
			background: url(../../static/node_bg_four.png) no-repeat;
			background-size: 100% 100%;
		}
	}
	.bottomBtn {
		position: fixed;
		left: 0;
		bottom: 0;
		width: 100%;
		height: 97rpx;
		font-size: 26rpx;
		.addNode {
			width: 469rpx;
			height: 97rpx;
			line-height: 97rpx;
			text-align: center;
			background-color: #1abb9b;
			border-radius: 0rpx 60rpx 0rpx 0rpx;
			color: #FFFFFF;
		}
	}
</style>
