<template>
	<view class="send">
		<view class="address">
			<view class="title">
				<view class="text">
					转账地址
				</view>
				<view class="btn">
					<view class="cut">
						剪贴板
					</view>
					<view class="qrCode">
						扫描二维码
					</view>
				</view>
			</view>
			<view class="input">
				<input type="text" placeholder-style="color:#999999" placeholder="请选择剪贴板或扫描二维码" v-model="inputClearValue" @input="clearInput" />
				<view class="uni-icon uni-icon-clear" v-if="showClearIcon" @click="clearIcon"></view>
			</view>
		</view>
		<view class="address">
			<view class="title">
				<view class="text">
					转账金额(WCL)
				</view>
			</view>
			<view class="input">
				<input type="text" placeholder-style="color:#999999" placeholder="请填写转账金额" v-model="inputClearValue" @input="clearInput" />
			</view>
		</view>
		<view class="address">
			<view class="title">
				<view class="text">
					备注信息(选填)
				</view>
			</view>
			<view class="input">
				<input type="text" placeholder-style="color:#999999" placeholder="请填写备注信息" v-model="inputClearValue" />
			</view>
		</view>
		<view class="address">
			<view class="title">
				<view class="text">
					手续费
				</view>
			</view>
			<view class="input">
				<input type="text" style="color:#1abb9b;" value="10.sat/byte" disabled/>
			</view>
		</view>
		<view class="bottomBtn">
			<view class="pay">
				支付
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				showClearIcon: false,
				inputClearValue:''
			}
		},
		onLoad() {

		},
		methods: {
			clearInput: function(event) {
				this.inputClearValue = event.target.value;
				if (event.target.value.length > 0) {
					this.showClearIcon = true;
				} else {
					this.showClearIcon = false;
				}
			},
			clearIcon: function() {
				this.inputClearValue = '';
				this.showClearIcon = false;
			},
		}
	}
</script>

<style lang="less">
	.send {
		height: 100%;
	}

	.address {
		padding: 60rpx 22rpx 0;

		.title {
			display: flex;
			justify-content: space-between;
			align-items: center;

			.text {
				font-size: 32rpx;
				color: #333333;
			}

			.btn {
				font-size: 26rpx;
				color: #FFFFFF;
				text-align: center;
				line-height: 46rpx;
				display: flex;

				.cut {
					width: 124rpx;
					height: 46rpx;
					background-color: #1abb9b;
					border-radius: 23rpx;
				}

				.qrCode {
					width: 175rpx;
					height: 46rpx;
					background-color: #1abb9b;
					border-radius: 23rpx;
					margin-left: 20rpx;
				}
			}
		}

		.input {
			margin-top: 20rpx;
			// width: 702rpx;
			height: 97rpx;
			background-color: #ebf8f5;
			border-radius: 30rpx;
			padding: 0 20rpx;
			box-sizing: border-box;
			display: flex;
			align-items: center;
			input{
				height: 100%;
				width: 100%;
			}
			.uni-icon-clear{
				padding: 10rpx;
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
		.pay {
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
