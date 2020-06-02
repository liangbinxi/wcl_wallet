<template>
	<view class="about">
		<view class="APPInfo">
			<image src="../../static/about_logo.png" mode=""></image>
			<view class="name">
				WCL Wallet
			</view>
			<view class="version">
				V3.3.8
			</view>
		</view>
		<view class="bottom">
			<view class="authorization">
				授权条款：MIT LICENCE
			</view>
			<view class="homePage">
				主页：www.90qkl.cn
			</view>
			<view class="text">
				vpub 开发
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
	
		}
	}
</script>

<style lang="less">
	.about{
		height: 100%;
		position: relative;
		text-align: center;
	}
	.APPInfo{
		padding-top: 200rpx;
		image{
			width: 156rpx;
			height: 137rpx;
		}
		.name{
			font-size: 40rpx;
			color: #333333;
			margin: 10rpx 0 20rpx;
		}
		.version{
			font-size: 26rpx;
			color: #1abb9b;
		}
	}
	.bottom{
		width: 100%;
		position: absolute;
		left: 0;
		bottom: 10px;
		font-size: 24rpx;
		color: #999999;
		text-align: center;
		.authorization{
			
		}
		.homePage{
			margin: 6rpx 0 16rpx;
		}
		.text{
			color: #c6c6c6;
		}
	}
</style>
