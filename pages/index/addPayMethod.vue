<template>
	<view class="addPayMethod">
		<view class="way-item bankCard" @click="onPageJump('/pages/index/addBankPayMethod')">
			<image src="../../static/icon_card_white.png" mode=""></image>
			<view class="title">
				银行卡
			</view>
		</view>
		<view class="way-item alipay" @click="onPageJump('/pages/index/addAlipayMethod')">
			<image src="../../static/icon_alipay_white.png" mode=""></image>
			<view class="title">
				支付宝
			</view>
		</view>
		<view class="way-item wechat" @click="onPageJump('/pages/index/addWechatPayMethod')">
			<image src="../../static/icon_wechat_white.png" mode=""></image>
			<view class="title">
				微信
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
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
	.addPayMethod{
		height: 100%;
		padding-top: 36rpx;
	}
	.way-item{
		width: 702rpx;
		height: 126rpx;
		border-radius: 30rpx;
		display: flex;
		align-items: center;
		margin: 0 auto;
		margin-bottom: 36rpx;
		image{
			width: 60rpx;
			height: 46rpx;
			margin: 0 34rpx;
		}
		.title{
			font-size: 30rpx;
			color: #FFFFFF;
		}
	}
	.bankCard{
		background-color: #ffc956;
		box-shadow: 0rpx 6rpx 11rpx 0rpx rgba(255, 201, 86, 0.53);
	}
	.alipay{
		background-color: #08a1f8;
		box-shadow: 0rpx 6rpx 11rpx 0rpx rgba(8, 161, 248, 0.53);
	}
	.wechat{
		background-color: #00c800;
		box-shadow: 0rpx 6rpx 11rpx 0rpx rgba(0, 200, 0, 0.53);
	}
</style>
