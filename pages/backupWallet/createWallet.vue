<template>
	<view class="createWallet">
		<view class="title">创建钱包</view>
		<view class="remind">钱包是存储数字资产的工具，更是一个生态的流量入口。随着生态中token经济生态的完善，使用场景会越来越多</view>
		<view class="newWallet imgBox">
			<view class="cnTitle">
				新钱包
			</view>
			<view class="enTitle">
				New wallet
			</view>
		</view>
		<view class="restoreWallet imgBox" @click="onPageJump('/pages/backupWallet/backupWalletOne')">
			<view class="cnTitle">
				恢复钱包
			</view>
			<view class="enTitle">
				Restore wallet
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
	.createWallet {
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
	.imgBox{
		width: 716rpx;
		height: 281rpx;
		margin: 0 auto;
		background: url(../../static/newwallet.png) no-repeat;
		background-size:100% 100%;
		color: #FFFFFF;
		box-sizing: border-box;
		padding: 60rpx 0 0 70rpx;
		.cnTitle{
			font-size: 46rpx;
		}
		.enTitle{
			font-size: 24rpx;
		}
	}
	.newWallet{
		
	}
	.restoreWallet{
		
	}
</style>
