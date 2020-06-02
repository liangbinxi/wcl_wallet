<template>
	<view class="setPW">
		<view class="title">设置钱包密码</view>
		<view class="remind">请设置一个钱包的密码</view>
		<view class="warn">用于支付或者特殊操作的验证</view>
		<view class="inputs">
			<input class="input" type="text" v-model="passWord" />
			<view class="inputBox" :class="{selected:passWord.length==0}">{{passWord.substr(0,1)}}</view>
			<view class="inputBox" :class="{selected:passWord.length==1}">{{passWord.substr(1,1)}}</view>
			<view class="inputBox" :class="{selected:passWord.length==2}">{{passWord.substr(2,1)}}</view>
			<view class="inputBox" :class="{selected:passWord.length==3}">{{passWord.substr(3,1)}}</view>
			<view class="inputBox" :class="{selected:passWord.length==4}">{{passWord.substr(4,1)}}</view>
			<view class="inputBox" :class="{selected:passWord.length==5}">{{passWord.substr(5,1)}}</view>
		</view>
		<view class="keypad">
			<view class="numBox" :class="{borderRight:index%3!==2,borderBottom:index<=8}" v-for="(item,index) in num" :key="index" @tap="numOperation(item)">
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
				passWord: '',
				num: ['1', '2', '3', '4', '5', '6', '7', '8', '9', , '0', 10]
			}
		},
		onLoad() {

		},
		methods: {
			numOperation(val) {
				console.log(val)
				// console.log(this.num)
				if (val === 10) {
					let str = this.passWord
					if (str.length === 0) return
					str = str.substr(0, str.length - 1)
					// console.log(str)
					this.passWord = str
					return
				}
				if (val&&this.passWord.length<6) {
					this.passWord = this.passWord + val
					if(this.passWord.length===6){
						console.log(this.passWord)
						uni.navigateTo({
							url: `/pages/backupWallet/confirmPassword?passWord=${this.passWord}`
						});
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
		.borderRight{
			border-right: 1px solid #eeeeee;
		}
		.borderBottom{
			border-bottom: 1px solid #eeeeee;
		}
	}
</style>
