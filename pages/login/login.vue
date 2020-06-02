<template>
	<view class="login">
		<view class="login_icon">
			<image src="../../static/login_icon_wallet.png" mode=""></image>
		</view>
		<view class="inputBox">
			<input type="text" value="" placeholder="请输入手机号码" />
		</view>
		<view class="inputBox pwInput">
			<input type="text" value="" placeholder="请输入密码" />
		</view>
		<view class="forgetPW">
			<text>忘记密码？</text>
		</view>
		<view class="bottomBtn">
			<view class="loginBtn" @click="loginJump('/pages/index/WCLWallet')">
				登录
			</view>
			<view class="goRegister" @click="onPageJump('/pages/register/register')">
				注册账号
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
			},
			loginJump(url) {
				uni.reLaunch({
					url: url
				});
			}
		}
	}
</script>

<style lang="less">
	.login {
		height: 100%;
		position: relative;
	}

	.login_icon {
		width: 232rpx;
		height: 225rpx;
		margin: 0 auto;
		padding-top: 150rpx;
		box-sizing: content-box;
		image {
			height: 100%;
			width: 100%;
		}
	}

	.inputBox {
		width: 670rpx;
		height: 97rpx;
		background-color: #ebf8f5;
		border-radius: 49rpx;
		margin: 220rpx auto 0;
		display: flex;
		justify-content: center;
		align-items: center;

		input {
			height: 100%;
			width: 80%;
		}
	}

	.pwInput {
		margin: 40rpx auto 0;
	}

	.forgetPW {
		margin: 40rpx auto 0;
		text-align: center;
		font-size: 26rpx;
		color: #333333;
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

		.loginBtn {
			width: 469rpx;
			height: 97rpx;
			line-height: 97rpx;
			text-align: center;
			background-color: #1abb9b;
			border-radius: 0rpx 60rpx 0rpx 0rpx;
			color: #FFFFFF;
		}

		.goRegister {
			height: 97rpx;
			flex: 1;
			line-height: 97rpx;
			text-align: center;
			color: #1abb9b;
		}
	}
</style>
