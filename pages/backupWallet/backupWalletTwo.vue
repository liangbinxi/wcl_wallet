<template>
	<view class="backup">
		<view class="title">钱包备份</view>
		<view class="remind">验证您的钱包助记词</view>
		<view class="warn">请根据您记下的助记词，按顺序填写，验证您备份的助记词无误。</view>
		<view class="textareaBox">
			<textarea class="textarea" value="" placeholder="" />
		</view>
		<view class="prompt">
			顺序或单词有误，请重新校对
		</view>
		<view class="bottomBtn">
			<view class="nextBtn" @click="onPageJump('/pages/backupWallet/setPassword')">
				下一步
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
			onPageJump(url) {
				uni.navigateTo({
					url: url
				});
			}
		}
	}
</script>

<style lang="less">
	.backup {
		height: 100%;
		position: relative;
	}

	.title {
		width: 670rpx;
		font-family: PingFang-SC-Bold;
		font-size: 60rpx;
		color: #333333;
		margin: 0 auto;
	}

	.remind {
		width: 670rpx;
		margin: 35rpx auto;
		font-size: 24rpx;
		color: #999999;
	}

	.warn {
		width: 670rpx;
		margin: 0 auto;
		color: #1bbc9c;
		font-size: 26rpx;
	}
	.textareaBox{
		width: 670rpx;
		height: 220rpx;
		margin: 100rpx auto 0;
		background-color: #1abb9b;
		border-radius: 30rpx;
		display: flex;
		justify-content: center;
		align-items: center;
		.textarea{
			height: 180rpx;
			width: 630rpx;
			color: #FFFFFF;
		}
	}
	.prompt{
		width: 428rpx;
			height: 71rpx;
			background-color: rgba(26, 187, 155, 0.2);
			border-radius: 30rpx;
			font-size: 26rpx;
			line-height: 71rpx;
			color: #1abb9b;
			text-align: center;
			position: absolute;
			left: 50%;
			bottom: 20%;
			transform: translateX(-50%);
	}
	.bottomBtn {
		position: fixed;
		left: 0;
		bottom: 0;
		width: 100%;
		height: 97rpx;
		display: flex;
		flex-direction: row;
		font-size: 26rpx;

		.nextBtn {
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
