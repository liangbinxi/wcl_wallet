<template>
	<view v-if="show" class="popup-input">
		<view :class="{'popup-mask':true,'popup-mask-ani':ani}"></view>
		<view class="popup-wrapper">
			<view :class="{popupBox:true,'popupBox-ani':ani}">
				<view class="head">
					<view class="title">
						标签
					</view>
					<image src="../static/icon_close.png" mode="" @tap="close()"></image>
				</view>
				<view class="inputBox">
					<input type="text" placeholder="请备注此交易标签" placeholder-style="color: #999999;" v-model="input" />
				</view>
				<view class="bottomBtn" @tap="save">
					保存
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				show:false,
				input:null,
				ani:false
			}
		},
		onLoad() {
	
		},
		methods: {
			open() {
				this.show = true
				this.$nextTick(() => {
					setTimeout(() => {
						this.ani =true
					}, 50)
				})
			},
			close() {
				this.ani =false
				this.$nextTick(function(){
					setTimeout(()=>{
						this.show = false
					},50)
				})
			},
			save(){
				this.$emit('save',{
					val:this.input
				})
				this.close()
			}
		}
	}
</script>

<style lang="less">
	.popup-input{
		position: fixed;
		top: 0;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
		z-index: 998;
		overflow: hidden
	}
	.popup-mask{
		position: absolute;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
		z-index: 998;
		background: rgba(0, 0, 0, .4);
		opacity: 0;
		transition: all .3s
	}
	.popup-mask-ani{
		opacity: 1;
	}
	.popup-wrapper{
		height: 100%;
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		.popupBox{
			opacity: 0;
			transition: all .3s;
			transform: scale(1,1.5);
			z-index: 999;
			width: 670rpx;
			background-color: #ffffff;
			border-radius: 30rpx;
			overflow: hidden;
			.head{
				display: flex;
				justify-content: space-between;
				align-items: center;
				padding: 20rpx 30rpx;
				.title{
					font-size: 36rpx;
					font-size: 36rpx;
				}
				image{
					width: 24rpx;
					height: 24rpx;
				}
			}
			.inputBox{
				width: 590rpx;
				height: 97rpx;
				background-color: #ebf8f5;
				border-radius: 30rpx;
				margin: 20rpx auto 40rpx;
				padding: 0 20rpx;
				input{
					height: 100%;
				}
			}
			.bottomBtn{
				height: 97rpx;
				background-color: #1abb9b;
				text-align: center;
				line-height: 97rpx;
				color: #FFFFFF;
			}
		}
		.popupBox-ani{
			// transition: all .3s;
			transform: scale(1);
			opacity: 1;
		}
	}

</style>
