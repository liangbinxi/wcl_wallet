<template>
	<view class="addAlipayMethod">
		<view class="input-item">
			<view class="title">
				真实姓名
			</view>
			<view class="inputBox">
				<input type="text" placeholder="请输入真实姓名" placeholder-style="color: #999999;" value="" />
			</view>
		</view>
		<view class="input-item">
			<view class="title">
				支付宝账号
			</view>
			<view class="inputBox">
				<input type="text" placeholder="请输入支付宝账号" placeholder-style="color: #999999;" value="" />
			</view>
		</view>
		<view class="bottomBtn">
			<view class="save">
				添加收款方式
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
	.addAlipayMethod{
		height: 100%;
	}
	.input-item{
		padding: 50rpx 22rpx 0;
		.title{
			font-size: 32rpx;
			color: #333333;
		}
		.inputBox{
			margin-top: 26rpx;
			height: 97rpx;
			background-color: #ebf8f5;
			border-radius: 30rpx;
			padding: 0 20rpx;
			input{
				height: 100%;
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
		.save {
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
