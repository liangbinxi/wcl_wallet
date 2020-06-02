<template>
	<view class="onChainFunds">
		<view class="fundList">
			<view class="header">
				<image src="../../static/funds_icon_funds.png" mode=""></image>
				<view class="title">
					<view class="cn">
						链上基金
					</view>
					<view class="en">
						On-chain funds
					</view>
				</view>
			</view>
			<view class="fund-item">
				<view class="name">
					社区基金余额
				</view>
				<view class="data">
					<view class="num">
						24,000,000.00
					</view>
					<view class="unit">
						WCL
					</view>
				</view>
			</view>
			<view class="fund-item">
				<view class="name">
					业绩基金余额
				</view>
				<view class="data">
					<view class="num">
						24,000,000.00
					</view>
					<view class="unit">
						WCL
					</view>
				</view>
			</view>
			<view class="fund-item">
				<view class="name">
					技术基金余额
				</view>
				<view class="data">
					<view class="num">
						24,000,000.00
					</view>
					<view class="unit">
						WCL
					</view>
				</view>
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
	
		}
	}
</script>

<style lang="less">
	.onChainFunds{
		height: 100%;
		position: relative;
		background: url(../../static/fund_bg.png)no-repeat;
		background-size: 100% 100%;
	}
	.fundList{
		color: #FFFFFF;
		font-size: 24rpx;
		padding:0 96rpx;
		.header{
			padding-top: 150rpx;
			display: flex;
			align-items: center;
			image{
				width: 96rpx;
				height: 65rpx;
			}
			.title{
				margin-left: 20rpx;
				.cn{
					font-size: 36rpx;
				}
				.en{
					
				}
			}
		}
		.fund-item{
			margin-top: 70rpx;
			.name{
				
			}
			.data{
				display: flex;
				justify-content: space-between;
				align-items: center;
				margin-top: 20rpx;
				.num{
					font-size: 60rpx;
				}
				.unit{
					font-size: 30rpx;
				}
			}
		}
	}
</style>
