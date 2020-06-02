<template>
	<view class="setPW">
		<view class="title">确认钱包密码</view>
		<view class="remind">再次确认设置的钱包密码</view>
		<view class="warn">用于支付或者特殊操作的验证</view>
		<view class="inputs">
			<input class="input" type="text" v-model="confirmPW" />
			<view class="inputBox" :class="{selected:confirmPW.length==0}">{{confirmPW.substr(0,1)}}</view>
			<view class="inputBox" :class="{selected:confirmPW.length==1}">{{confirmPW.substr(1,1)}}</view>
			<view class="inputBox" :class="{selected:confirmPW.length==2}">{{confirmPW.substr(2,1)}}</view>
			<view class="inputBox" :class="{selected:confirmPW.length==3}">{{confirmPW.substr(3,1)}}</view>
			<view class="inputBox" :class="{selected:confirmPW.length==4}">{{confirmPW.substr(4,1)}}</view>
			<view class="inputBox" :class="{selected:confirmPW.length==5}">{{confirmPW.substr(5,1)}}</view>
		</view>
		<view class="warnBox" v-show="warning&&confirmPW.length===6">
			钱包密码填写不相同
		</view>
		<view class="keypad">
			<view class="numBox" :class="{borderRight:index%3!==2,borderBottom:index<=8}" v-for="(item,index) in num" :key="index"
			 @tap="numOperation(item)">
				{{item===10?'':item}}
				<image v-if="item===10" src="../../static/back.jpg" mode=""></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				warning:false,
				passWord:'',
				confirmPW: '',
				num: ['1', '2', '3', '4', '5', '6', '7', '8', '9', , '0', 10]
			}
		},
		onLoad(option) {
			this.passWord = option.passWord
		},
		methods: {
			numOperation(val) {
				if (val === 10) {
					let str = this.confirmPW
					if (str.length === 0) return
					str = str.substr(0, str.length - 1)
					this.confirmPW = str
					return
				}
				if (val&&this.confirmPW.length<6) {
					this.warning = false
					this.confirmPW = this.confirmPW + val
					if(this.confirmPW.length===6){
						console.log(this.confirmPW)
						if(this.confirmPW === this.passWord){
							console.log('密码一样')
							return
						}
						this.warning = true
						// uni.navigateTo({
						// 	url: `/pages/backupWallet/confirmPassword?passWord=${this.passWord}`
						// });
					}
				}
			}
		}
	}
</script>

<style lang="less">
	.setPW {
		height: 100%;
		position: relative;
	}

	.title {
		width: 670rpx;
		font-family: PingFang-SC-Bold;
		font-size: 60rpx;
		color: #333333;
		margin: 0 auto;
	}

	.remind {
		width: 670rpx;
		margin: 35rpx auto;
		font-size: 24rpx;
		color: #999999;
	}

	.warn {
		width: 670rpx;
		margin: 0 auto;
		color: #1bbc9c;
		font-size: 26rpx;
	}

	.inputs {
		position: relative;
		width: 670rpx;
		display: flex;
		margin: 80rpx auto 0;
		justify-content: space-between;
		align-items: center;

		.input {
			position: absolute;
			width: 100%;
			height: 100%;
			opacity: 0;
		}

		.inputBox {
			width: 80rpx;
			height: 84rpx;
			border-radius: 10rpx;
			background-color: rgba(26, 187, 155, 0.2);
			text-align: center;
			line-height: 84rpx;
			box-sizing: border-box;
		}

		.selected {
			border: 1px solid #1abb9b;
		}
	}

	.warnBox {
		position: absolute;
		left: 50%;
		bottom: 50%;
		width: 428rpx;
		height: 71rpx;
		background-color: rgba(26, 187, 155, 0.2);
		border-radius: 30rpx;
		transform: translateX(-50%);
		text-align: center;
		font-size: 26rpx;
		line-height: 71rpx;
		color: #1abb9b;
	}

	.keypad {
		position: absolute;
		left: 0;
		bottom: 0;
		box-sizing: border-box;
		height: 40%;
		width: 100%;
		display: flex;
		flex-wrap: wrap;
		border-top: 1px solid #eeeeee;

		.numBox {
			box-sizing: border-box;
			width: 33.33%;
			height: 25%;
			display: flex;
			justify-content: center;
			align-items: center;

			image {
				width: 35rpx;
				height: 29rpx;
			}
		}

		.borderRight {
			border-right: 1px solid #eeeeee;
		}

		.borderBottom {
			border-bottom: 1px solid #eeeeee;
		}
	}
</style>
