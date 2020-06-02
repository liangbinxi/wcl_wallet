<template>
	<view class="wallet">
		<view class="top">
			<view class="menu" @click="drawerShow=true">
				<image src="../../static/wallet_icon_menu.png" mode=""></image>
			</view>
		</view>
		<view class="name">
			<view class="text">
				WCL Wallet
			</view>
			<image @tap="openInputBox" src="../../static/wallet_icon_rename_black.png" mode=""></image>
		</view>
		<view class="assets">
			<view class="topTitle">
				<text>我的总资产</text>
				<image src="../../static/wallet_icon_logo.png" mode=""></image>
			</view>
			<view class="numWCL">
				<text class="num">1986.9998348</text>
				<text class="wcl">WCL</text>
			</view>
			<view class="money">
				0.0124172￥
			</view>
			<view class="btns">
				<view class="out btn" @click="onPageJump('/pages/index/send')">
					<image src="../../static/wallet_icon_send.png" mode=""></image>
					<text>发出</text>
				</view>
				<view class="in btn" @click="onPageJump('/pages/index/receive')">
					<image src="../../static/wallet_icon_receive.png" mode=""></image>
					<text>接收</text>
				</view>
				<view class="main btn" @click="onPageJump('/pages/index/masterNode')">
					<image src="../../static/wallet_icon_node.png" mode=""></image>
					<text>主节点</text>
				</view>
			</view>
		</view>
		<view class="lists">
			<scroll-view scroll-y="true" style="height: 100%;">
			<view class="item" @click="onPageJump('/pages/index/dealDetails')">
				<image src="../../static/wallet_icon_send_red.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						-10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_send_red.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						-10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_send_red.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						-10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_receive_green.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						+10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_receive_green.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						+10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_send_red.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						-10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_send_red.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						-10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_send_red.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						-10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_send_red.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						-10.0000452
					</view>
				</view>
			</view>
			<view class="item">
				<image src="../../static/wallet_icon_send_red.png" mode=""></image>
				<view class="rightInfo">
					<view class="info">
						<view class="title">
							钱包发送WCL
						</view>
						<view class="time">
							2020-04-14 12:01
						</view>
					</view>
					<view class="num">
						-10.0000452
					</view>
				</view>
			</view>
			</scroll-view>
		</view>
		<drawer :visible="drawerShow" mode="left" @close="closeDrawer()">
			<view class="walletTitle">
				WCL Wallet
			</view>
			<view class="navigationList">
				<view class="item" @click="onPageJump('/pages/index/about')">关于</view>
				<view class="item" @click="onPageJump('/pages/index/wallet')">钱包</view>
				<view class="item">网络</view>
				<view class="item" @click="onPageJump('/pages/index/cash')">兑现</view>
				<view class="item">账户</view>
				<view class="item">收款账户</view>
				<view class="item" @click="onPageJump('/pages/index/onChainFunds')">链上公示</view>
				<view class="item">退出账户</view>
			</view>
		</drawer>
		<popup-input ref='popupInput' @save="save"></popup-input>
	</view>
</template>

<script>
	import drawer from '@/components/drawer.vue'
	import popupInput from '../../components/popup-input.vue'
	export default {
		components: {
			drawer,
			popupInput
		},
		data() {
			return {
				drawerShow:false
			}
		},
		onLoad() {
	
		},
		onHide(){
			this.drawerShow = false
		},
		methods: {
			closeDrawer(){
				this.drawerShow = false
			},
			onPageJump(url) {
				uni.navigateTo({
					url: url
				});
			},
			openInputBox(){
				this.$refs.popupInput.open()
			},
			save(val){
				console.log(val)
			}
		}
	}
</script>

<style lang="less">
	.wallet{
		height: 100%;
		position: relative;
		display: flex;
		flex-direction: column;
	}
	.top{
		height: 80rpx;
		display: flex;
		align-items: center;
		.menu{
			padding: 30rpx 30rpx 0;
			height: 100%;
			image{
				width: 33rpx;
				height: 21rpx;
			}
		}
	}
	.name{
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 0 22rpx;
		margin: 20rpx 0 50rpx;
		.text{
			font-size: 40rpx;
			color: #333333;
		}
		image{
			width: 35rpx;
			height: 35rpx;
		}
	}
	.assets{
		padding: 0 22rpx;
		height: 308rpx;
		background: url(../../static/wallet_assets.png) no-repeat;
		background-size: 100% 100%;
		color: #FFFFFF;
		.topTitle{
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 30rpx 40rpx 0;
			text{
				font-size: 24rpx;
			}
			image{
				width: 40rpx;
				height: 35rpx;
			}
		}
		.numWCL{
			padding: 0 40rpx;
			font-size: 26rpx;
			.num{
				font-size: 46rpx;
			}
			.wcl{
				margin-left: 20rpx;
			}
		}
		.money{
			padding: 0 40rpx;
			font-size: 24rpx;
		}
		.btns{
			display: flex;
			justify-content: space-around;
			align-items: center;
			margin-top: 14rpx;
			height: 76rpx;
			.btn{
				font-size: 24rpx;
				width: 33.33%;
				display: flex;
				justify-content: center;
				align-items: center;
				height: 76rpx;
				image{
					height: 23rpx;
					width: 23rpx;
					margin-right: 10rpx;
				}
			}
			.in{
				border-left: 1px solid #FFFFFF;
				border-right: 1px solid #FFFFFF;
			}
		}
	}
	.lists{
		
		height: 500rpx;
		// display: flex;
		// flex-direction: column;
		flex: 1;
		.item{
			display: flex;
			justify-content: space-between;
			align-items: center;
			margin-bottom: 30rpx;
			padding: 0 22rpx;
			image{
				width: 70rpx;
				height: 70rpx;
			}
			.rightInfo{
				color: #333333;
				font-size: 28rpx;
				flex: 1;
				display: flex;
				justify-content: space-between;
				align-items: center;
				margin-left: 20rpx;
				.info{
					.title{
						font-size: 26rpx;
					}
					.time{
						font-size: 24rpx;
					}
				}
				.num{
					
				}
			}
		}
	}
	.walletTitle{
		font-size: 40rpx;
		color: #333333;
		margin: 50rpx 0;
		text-align: center;
	}
	.navigationList{
		font-size: 28rpx;
		color: #666666;
		padding-left: 80rpx;
		.item{
			padding: 30rpx 0;
		}
	}
</style>
