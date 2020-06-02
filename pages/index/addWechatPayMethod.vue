<template>
	<view class="addWechatPayMethod">
		<view class="input-item">
			<view class="title">
				微信昵称
			</view>
			<view class="inputBox">
				<input type="text" placeholder="请输入微信昵称" placeholder-style="color: #999999;" value="" />
			</view>
		</view>
		<view class="input-item">
			<view class="title">
				微信账号
			</view>
			<view class="inputBox">
				<input type="text" placeholder="请输入微信账号" placeholder-style="color: #999999;" value="" />
			</view>
		</view>
		<view class="input-item">
			<view class="title">
				微信收款码
			</view>
			<view class="photoBox" v-if="imageList.length!=0">
				<image :src="imageList[0]" :data-src="imageList[0]" mode="" @tap="previewImage"></image>
				<view class="close" @tap="close">
					<image src="../../static/icon_close.png" mode=""></image>
				</view>
			</view>
			<view class="addBox" v-if="imageList.length==0" @tap="chooseImage">
				<image src="../../static/cash_icon_add.png" mode=""></image>
			</view>
		</view>
		<view class="bottomBtn">
			<view class="save">
				保存
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imageList:[]
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
			close(){
				this.imageList = []
			},
			chooseImage:function() {
				uni.chooseImage({
					sourceType: ['album'],
					sizeType: ['original', 'compressed'],
					count: 1,
					success: (res) => {
						console.log(res)
						this.imageList = this.imageList.concat(res.tempFilePaths);
					},
					fail: (err) => {
						console.log(err)
					}
				})
			},
			previewImage: function(e) {
				console.log(e)
				var current = e.target.dataset.src
				uni.previewImage({
					current: current,
					urls: this.imageList
				})
			}
		}
	}
</script>

<style lang="less">
	.addWechatPayMethod{
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
		.photoBox{
			position: relative;
			margin-top: 26rpx;
			width: 300rpx;
			height: 300rpx;
			border-radius: 30rpx;
			overflow: hidden;
			image{
				height: 100%;
				width: 100%;
			}
			.close{
				position: absolute;
				right: 2%;
				top: 2%;
				height: 40rpx;
				width: 40rpx;
				border-radius: 50%;
				display: flex;
				justify-content: center;
				align-items: center;
				background: rgba(51,51,51,0.5);
				overflow: hidden;
				padding: 10rpx;
			}
		}
		.addBox{
			margin-top: 26rpx;
			width: 300rpx;
			height: 300rpx;
			background-color: #ebf8f5;
			border-radius: 30rpx;
			display: flex;
			justify-content: center;
			align-items: center;
			image{
				height: 46rpx;
				width: 46rpx;
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
