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
		<view class="getCode">
			<view class="codeInput">
				<input type="text" value="" placeholder="请输入验证码" />
			</view>
			<view class="getCodeBtn">
				获取验证码
			</view>
		</view>
		<view class="bottomBtn">
			<view class="loginBtn">
				注册账号
			</view>
			<view class="goRegister" @click="onPageJump('/pages/login/login')">
				返回登录
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

	.getCode {
		width: 670rpx;
		height: 97rpx;
		margin: 40rpx auto 0;
		display: flex;
		justify-content: space-between;
		font-size: 26rpx;

		.codeInput {
			height: 100%;
			width: 400rpx;
			background-color: #ebf8f5;
			border-radius: 49rpx;
			display: flex;
			justify-content: center;
			// align-items: center;
			// margin: 0 auto;
			input {
				height: 100%;
				width: 70%;
			}
		}

		.getCodeBtn {
			width: 240rpx;
			height: 97rpx;
			background-color: #1abb9b;
			border-radius: 49rpx;
			line-height: 97rpx;
			text-align: center;
			color: #ffffff;
		}
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
