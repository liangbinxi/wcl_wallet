<template>
	<view class="details">
		<view class="headerBox">
			<view class="text">
				<image src="../../static/detail_icon_bigsend.png" mode=""></image>
				<text>发送WCL(劳务费）</text>
			</view>
			<view class="num">
				1986.999
			</view>
			<view class="money">
				0.0124172￥ 
			</view>
		</view>
		<view class="infoBox">
			<view class="infoList">
				<view class="item">
					<view class="text">
						交易时间
					</view>
					<view class="num">
						2020-04-14 12:01
					</view>
				</view>
				<view class="item">
					<view class="text">
						交易类型
					</view>
					<view class="num">
						转账
					</view>
				</view>
				<view class="item">
					<view class="text">
						发送地址
					</view>
					<view class="num">
						30123asdzxca112Esaz112314141sd122zcz1213e
					</view>
				</view>
				<view class="item">
					<view class="text">
						接收地址
					</view>
					<view class="num">
						30123asdzxca112Esaz112314141sd122zcz1213e
					</view>
				</view>
				<view class="item">
					<view class="text">
						手续费
					</view>
					<view class="num">
						0.000001 WCL
					</view>
				</view>
				<view class="item">
					<view class="text">
						交易单号
					</view>
					<view class="num">
						012015465610
					</view>
				</view>
			</view>
		</view>
		<popup-input ref='popupInput' @save="save"></popup-input>
	</view>
</template>

<script>
	import popupInput from '../../components/popup-input.vue'
	export default {
		components:{
			popupInput
		},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {
	
		},
		onNavigationBarButtonTap(e) {
			console.log(e)
			this.$refs.popupInput.open()
		},
		methods: {
			save(val){
				console.log(val)
			}
		}
	}
</script>

<style lang="less">
	.details{
		height: 100%;
		position: relative;
	}
	.headerBox{
		height: 455rpx;
		background: url(../../static/detail_bg.png) no-repeat;
		background-size: 100% 100%;
		background-position: 100% 50%;
		color: #FFFFFF;
		padding: 0 22rpx;
		.text{
			font-size: 30rpx;
			padding-top: 160rpx;
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
		margin-top: -60rpx;
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
</style>
