<template>
	<view class="receive">
		<view style="height: 1px;"></view>
		<view class="header">
			<view class="name">
				23axza1e1zxdaczxc11223axza1e1zxdaczxc112
			</view>
			<view class="icon">
				<image style="margin-right: 30rpx;" src="../../static/receive_icon_copy.png" mode=""></image>
				<image src="../../static/receive_icon_share.png" mode=""></image>
			</view>
		</view>
		<view class="mid">
			<view class="title">
				转账金额(WCL)
			</view>
			<view class="input">
				<input type="text" value="" />
			</view>
			<view class="title">
				备注信息
			</view>
			<view class="input">
				<input type="text" value="" />
			</view>
		</view>
		<view class="bottom">
			<image src="../../static/about_logo.png" mode=""></image>
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

		}
	}
</script>

<style lang="less">
	.receive {
		height: 100%;
		background: #1abb9b;
		position: relative;
	}

	.header {
		display: flex;
		flex-direction: column;
		justify-content: center;
		height: 190rpx;
		width: 702rpx;
		background: #FFFFFF;
		border-radius: 30rpx 30rpx 15rpx 15rpx;
		margin: 50rpx auto 0;
		// padding-top: 50rpx;
		// box-sizing: content-box;
		.name {
			font-size: 26rpx;
			color: #333333;
			font-weight: bold;
			text-align: center;
			margin: 0 auto;
			overflow: hidden;
			/*超出部分隐藏*/
			text-overflow: ellipsis;
			/* 超出部分显示省略号 */
			white-space: nowrap;
			/*规定段落中的文本不进行换行 */
			width: 323rpx;
			/*需要配合宽度来使用*/
		}

		.icon {
			display: flex;
			justify-content: center;
			align-items: center;
			margin-top: 20rpx;

			image {
				width: 28rpx;
				height: 28rpx;
			}
		}
	}

	.mid {
		background: #FFFFFF;
		margin: 0 auto;
		width: 702rpx;
		height: 484rpx;
		padding: 0 20rpx;
		border-radius: 15rpx;
		border-top: 1px dashed #1abb9b;
		border-bottom: 1px dashed #1abb9b;

		.title {
			font-size: 32rpx;
			color: #333333;
			padding: 35rpx 0;
		}

		.input {
			display: flex;
			align-items: center;
			// width: 646rpx;
			height: 97rpx;
			background-color: #ebf8f5;
			border-radius: 30rpx;
			padding: 0 20rpx;

			input {
				height: 100%;
				width: 100%;
			}

		}
	}
	.bottom{
		height: 434rpx;
		width: 702rpx;
		display: flex;
		justify-content: center;
		align-items: center;
		background: #FFFFFF;
		margin: 0 auto;
		border-radius: 15rpx 15rpx 30rpx 30rpx;
		image{
			width: 315rpx;
				height: 315rpx;
		}
	}
</style>
