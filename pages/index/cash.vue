<template>
	<view class="cash">
		<view class="cashRMB">
			<view class="text">
				<view class="title">
					兑现金额(RMB)
				</view>
				<view class="remaining">
					余额:1986.999
				</view>
			</view>
			<view class="inputBox">
				<input type="text" placeholder="请输入要兑现的金额" placeholder-style="color: #999999;" value="" />
			</view>
		</view>
		<view class="PayMethods">
			<view class="text">
				<view class="title">
					选择收款方式
				</view>
				<view class="add" @click="onPageJump('/pages/index/payMethod')">
					<image src="../../static/cash_icon_add.png" mode=""></image>
				</view>
			</view>
			
		</view>
		<view class="PayMethodList">
			<scroll-view scroll-y="true" style="height: 100%;">
				<view class="itemList">
					<view :class="{'pay-item':true ,'selected-pay-item':index==0}" @tap="index=0">
						<view class="icon">
							<image :src="index==0?'../../static/icon_alipay_white.png':'../../static/icon_alipay.png'" mode=""></image>
						</view>
						<view class="pay-text">
							<view class="wayName">
								支付宝
							</view>
							<view class="name">
								迪丽热巴
							</view>
						</view>
					</view>
					<view :class="{'pay-item':true ,'selected-pay-item':index==1}" @tap="index=1">
						<view class="icon">
							<image :src="index==1?'../../static/icon_wechat_white.png':'../../static/icon_wechat.png'" mode=""></image>
						</view>
						<view class="pay-text">
							<view class="wayName">
								微信
							</view>
							<view class="name">
								汤姆
							</view>
						</view>
					</view>
					<view :class="{'pay-item':true ,'selected-pay-item':index==2}" @tap="index=2">
						<view class="icon">
							<image :src="index==2?'../../static/icon_card_white.png':'../../static/icon_card.png'" mode=""></image>
						</view>
						<view class="pay-text">
							<view class="wayName">
								银行卡-招商银行
							</view>
							<view class="name">
								迪丽热巴
							</view>
						</view>
					</view>
					
				</view>
			</scroll-view>
		</view>
		<view class="bottomBtn">
			<view class="payNew">
				立即兑现
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				index:null
			}
		},
		onLoad() {
	
		},
		onNavigationBarButtonTap(e) {
			console.log(e)
			this.onPageJump('/pages/index/cashRecords')
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
	.cash{
		height: 100%;
		position: relative;
		display: flex;
		flex-direction: column;
	}
	.cashRMB{
		padding: 0 22rpx;
		.text{
			display: flex;
			justify-content: space-between;
			align-items: flex-end;
			padding: 38rpx 0 22rpx;
			.title{
				font-size: 32rpx;
				color: #333333;
			}
			.remaining{
				font-size: 26rpx;
				color: #1abb9b;
			}
		}
		.inputBox{
			width: 702rpx;
			height: 97rpx;
			background-color: #ebf8f5;
			border-radius: 30rpx;
			padding: 0 36rpx;
			input{
				height: 100%;
				width: 100%;
			}
		}
	}
	.PayMethods{
		margin-top: 80rpx;
		padding: 0 22rpx;
		color: #333333;
		font-size: 26rpx;
		.text{
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding-bottom: 32rpx;
			.title{
				font-size: 32rpx;
			}
			.add{
				width: 32rpx;
				height: 32rpx;
				image{
					width: 32rpx;
					height: 32rpx;
				}
			}
		}
		
	}
	.PayMethodList{
		flex: 1;
		height: 300rpx;
		// padding: 0 22rpx;
		.itemList{
			padding-bottom: 80rpx;
			.pay-item{
				margin: 0 auto;
				margin-bottom: 16rpx;
				// padding: 30rpx 0;
				height: 130rpx;
				width: 702rpx;
				background-color: #ebf8f5;
				border-radius: 30rpx;
				display: flex;
				align-items: center;
				color: #333333;
				font-size: 26rpx;
				.icon{
					margin-left: 30rpx;
					width: 60rpx;
					height: 46rpx;
					image{
						width: 60rpx;
						height: 46rpx;
					}
				}
				.pay-text{
					margin-left: 22rpx;
					.wayName{
						
					}
					.name{
						color: #999999;
					}
				}
			}
			.selected-pay-item{
				background-color: #1abb9b;
				color: #FFFFFF;
				.pay-text{
					.name{
						color: #FFFFFF;
					}
				}
			}
		}
		
	}
	.bottomBtn {
		position: fixed;
		left: 0;
		bottom: 0;
		width: 100%;
		height: 97rpx;
		font-size: 26rpx;
		.payNew {
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
