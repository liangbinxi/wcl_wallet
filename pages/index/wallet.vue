
<template>
	<view class="wallet">
		<scroll-view scroll-y="true" style="height: 100%;">
			<view class="walletList">
				<view class="wallet-item">
					<view class="name">
						WCL Wallet
					</view>
					<view class="num">
						123456.654321
					</view>
				</view>
				<view class="wallet-item">
					<view class="name">
						Iucccc
					</view>
					<view class="num">
						123456.654321
					</view>
				</view>
				<view class="wallet-item">
					<view class="name">
						WCL Wallet2
					</view>
					<view class="num">
						123456.654321
					</view>
				</view>
				<view class="wallet-item">
					<view class="name">
						WCL Wallet3
					</view>
					<view class="num">
						123456.654321
					</view>
				</view>
				<view class="wallet-item">
					<view class="name">
						WCL Wallet4
					</view>
					<view class="num">
						123456.654321
					</view>
				</view>
				<view class="wallet-item">
					<view class="name">
						WCL Wallet5
					</view>
					<view class="num">
						123456.654321
					</view>
				</view>
			</view>
		</scroll-view>
		<view class="bottomBtn" @click="onPageJump('/pages/backupWallet/createWallet')">
			<view class="createWallet">
				创建钱包
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
		onNavigationBarButtonTap(e) {
			console.log(e)
			
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
	.wallet{
		height: 100%;
		position: relative;
	}
	.walletList{
		// height: 100%;
		color: #FFFFFF;
		padding: 50rpx 0;
		.wallet-item{
			width: 716rpx;
			height: 281rpx;
			// background: url(../../static/wallet_bg_one.png) no-repeat;
			// background-size: 100% 100%;
			margin: 0 auto;
			margin-top: -36rpx;
			padding: 70rpx 60rpx;
			.name{
				font-size: 38rpx;
			}
			.num{
				font-size: 24rpx;
			}
		}
		.wallet-item:nth-child(4n+1){
			background: url(../../static/wallet_bg_one.png) no-repeat;
			background-size: 100% 100%;
		}
		.wallet-item:nth-child(4n+2){
			background: url(../../static/wallet_bg_two.png) no-repeat;
			background-size: 100% 100%;
		}
		.wallet-item:nth-child(4n+3){
			background: url(../../static/wallet_bg_three.png) no-repeat;
			background-size: 100% 100%;
		}
		.wallet-item:nth-child(4n+4){
			background: url(../../static/wallet_bg_four.png) no-repeat;
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
		.createWallet {
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