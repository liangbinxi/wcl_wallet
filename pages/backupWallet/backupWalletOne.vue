<template>
	<view class="backup">
		<view class="title">钱包备份</view>
		<view class="remind">请记录好生成的助记词，记录好助记词后，点击下一步。</view>
		<view class="warn">注意：助记词是用户钱包的唯一标识，不能分享给他人，严格保密。掌握该助记词的用户即可控制该钱包。</view>
		<view class="textareaBox">
			<textarea class="textarea" value="" placeholder="" />
		</view>
		<view class="bottomBtn">
			<view class="nextBtn" @click="onPageJump('/pages/backupWallet/backupWalletTwo')">
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
		margin: 100rpx auto;
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
