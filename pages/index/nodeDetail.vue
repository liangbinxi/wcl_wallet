<template>
	<view class="details">
		<view class="headerBox">
			<view class="text">
				<image src="../../static/detail_icon_bignode.png" mode=""></image>
				<text>MN-684</text>
			</view>
			<view class="num">
				123.321
			</view>
			<view class="money">
				0.0124172￥ 
			</view>
		</view>
		<view class="infoBox">
			<view class="infoList">
				<view class="item">
					<view class="text">
						激活时间
					</view>
					<view class="num">
						2020-04-14 12:01
					</view>
				</view>
				<view class="item">
					<view class="text">
						收益地址
					</view>
					<view class="num">
						30123asdzxca112Esaz112314141sd122zcz1213e
					</view>
				</view>
				<view class="item">
					<view class="text">
						交易信息
					</view>
					<view class="num">
						30123asdzxca112Esaz112314141sd122zcz1213e
					</view>
				</view>
				<view class="item">
					<view class="text">
						节点私钥
					</view>
					<view class="num">
						30123asdzxca112Esaz112314141sd122zcz1213e
					</view>
				</view>
				<view class="item">
					<view class="text">
						节点IP
					</view>
					<view class="num">
						52.82.101.206:9069
					</view>
				</view>
				
			</view>
		</view>
		<view class="nodeIncomeList">
			<scroll-view scroll-y="true" style="height: 100%;">
				<view class="income-item">
					<view class="left">
						<image src="../../static/wallet_icon_receive_green.png" mode=""></image>
						<view class="text">
							<view class="name">
								钱包接收WCL
							</view>
							<view class="time">
								2020-04-14 12:01
							</view>
						</view>
					</view>
					<view class="right">
						+10.0000452
					</view>
				</view>
				<view class="income-item">
					<view class="left">
						<image src="../../static/wallet_icon_receive_green.png" mode=""></image>
						<view class="text">
							<view class="name">
								钱包接收WCL
							</view>
							<view class="time">
								2020-04-14 12:01
							</view>
						</view>
					</view>
					<view class="right">
						+10.0000452
					</view>
				</view>
				<view class="income-item">
					<view class="left">
						<image src="../../static/wallet_icon_receive_green.png" mode=""></image>
						<view class="text">
							<view class="name">
								钱包接收WCL
							</view>
							<view class="time">
								2020-04-14 12:01
							</view>
						</view>
					</view>
					<view class="right">
						+10.0000452
					</view>
				</view>
				<view class="income-item">
					<view class="left">
						<image src="../../static/wallet_icon_receive_green.png" mode=""></image>
						<view class="text">
							<view class="name">
								钱包接收WCL
							</view>
							<view class="time">
								2020-04-14 12:01
							</view>
						</view>
					</view>
					<view class="right">
						+10.0000452
					</view>
				</view>
				<view class="income-item">
					<view class="left">
						<image src="../../static/wallet_icon_receive_green.png" mode=""></image>
						<view class="text">
							<view class="name">
								钱包接收WCL
							</view>
							<view class="time">
								2020-04-14 12:01
							</view>
						</view>
					</view>
					<view class="right">
						+10.0000452
					</view>
				</view>
			</scroll-view>
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
	.details{
		height: 100%;
		position: relative;
		display: flex;
		flex-direction: column;
	}
	.headerBox{
		height: 350rpx;
		background: url(../../static/detail_bg.png) no-repeat;
		background-size: 100% 100%;
		background-position: 100% 50%;
		color: #FFFFFF;
		padding: 0 22rpx;
		.text{
			font-size: 30rpx;
			padding-top: 50rpx;
			image{
				width: 41rpx;
				height: 42rpx;
				margin-right: 20rpx;
			}
		}
		.num{
			font-size: 70rpx;
			font-family: PingFang-SC-Medium;
			margin: 10rpx 0;
		}
		.money{
			font-size: 24rpx;
		}
	}
	.infoBox{
		width: 702rpx;
		// height: 718rpx;
		background-color: #ffffff;
		border-radius: 30rpx;
		box-shadow: 0rpx 7rpx 14rpx 4rpx 
				rgba(155, 168, 165, 0.14);
		// position: absolute;
		// left: 50%;
		// top: 300rpx;
		// transform: translateX(-50%);
		margin: 0 auto;
		// padding: 10rpx 0;
		margin-top: -50rpx;
		.infoList{
			padding: 0 26rpx;
			.item{
				padding: 20rpx 0;
				.text{
					font-size: 32rpx;
					color: #333333;
				}
				.num{
					font-size: 24rpx;
					color: #999999;
				}
			}
		}
	}
	.nodeIncomeList{
		height: 300rpx;
		flex: 1;
		.income-item{
			padding: 20rpx 22rpx;
			display: flex;
			justify-content: space-between;
			align-items: center;
			color: #333333;
			.left{
				display: flex;
				align-items: center;
				image{
					width: 70rpx;
					height: 70rpx;
				}
				.text{
					margin-left: 24rpx;
					.name{
						font-size: 26rpx;
					}
					.time{
						font-size: 26rpx;
					}
				}
			}
			.right{
				font-size: 28rpx;
			}
		}
	}
</style>
