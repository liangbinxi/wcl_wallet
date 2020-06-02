<template>
	<view class="masterNodeCreate">
		<view class="address">
			<view class="title">
				<view class="text">
					节点名称
				</view>
				
			</view>
			<view class="input">
				<input type="text" v-model="inputClearValue" @input="clearInput" />
				<view class="uni-icon uni-icon-clear" v-if="showClearIcon" @click="clearIcon"></view>
			</view>
		</view>
		<view class="address">
			<view class="title">
				<view class="text">
					质押交易
				</view>
				<view class="btn">
					<view class="select" @click="popupShow('deal')">
						选择
					</view>
				</view>
			</view>
			<view class="input">
				<input type="text" />
			</view>
			<view class="input">
				<input type="text" />
			</view>
		</view>
		<view class="address">
			<view class="title">
				<view class="text">
					主节点
				</view>
				<view class="btn">
					<view class="select" @click="popupShow('masterNode')">
						选择
					</view>
				</view>
			</view>
			<view class="input">
				<input type="text" placeholder="请选择主节点" placeholder-style="color: #999999;" />
			</view>
			<view class="input">
				<input type="text" placeholder="请选择主节点" placeholder-style="color: #999999;"/>
			</view>
		</view>
		<view class="bottomBtn">
			<view class="pay" @tap="activation">
				激活
			</view>
			<view class="goRegister">
				重置信息
			</view>
		</view>
		<uni-popup ref="deal" type="bottom" :custom="true">
			<view class="popup-bottom">
				<view class="title">
					<text class="text">质押交易</text>
					<text class="cancel" @click="popupHide('deal')">取消</text>
				</view>
				<view class="item">
					<view class="head">
						<view class="info">
							<view class="icon">
								<image src="../../static/node_icon_receive_white.png" mode=""></image>
							</view>
							<view class="name">
								<view class="text">23axza1e1zx...daczxc112</view>
								<view class="note">未备注</view>
							</view>
						</view>
						<view class="del">
							<image src="../../static/icon_close_white.png" mode=""></image>
						</view>
					</view>
					<view class="item-select">
						<view class="select">
							选择
						</view>
					</view>
				</view>
				<view class="item used">
					<view class="head">
						<view class="info">
							<view class="icon">
								<image src="../../static/node_icon_receive_white.png" mode=""></image>
							</view>
							<view class="name">
								<view class="text">23axza1e1zx...daczxc112</view>
								<view class="note">未备注</view>
							</view>
						</view>
						<view class="del">
							<image src="../../static/icon_close_white.png" mode=""></image>
						</view>
					</view>
					<view class="item-select">
						<view class="text-used">
							已使用
						</view>
					</view>
				</view>
				<view class="item">
					<view class="head">
						<view class="info">
							<view class="icon">
								<image src="../../static/node_icon_receive_white.png" mode=""></image>
							</view>
							<view class="name">
								<view class="text">23axza1e1zx...daczxc112</view>
								<view class="note">未备注</view>
							</view>
						</view>
						<view class="del">
							<image src="../../static/icon_close_white.png" mode=""></image>
						</view>
					</view>
					<view class="item-select">
						<view class="select">
							选择
						</view>
					</view>
				</view>
				<view class="rescanBtn">
					<view class="Btn">
						<image src="../../static/node_scancode.png" mode=""></image>
						<text>重新扫描</text>
					</view>
				</view>
			</view>
		</uni-popup>
		<uni-popup ref="masterNode" type="bottom" :custom="true">
			<view class="popup-bottom">
				<view class="title">
					<text class="text">主节点</text>
					<text class="cancel" @click="popupHide('masterNode')">取消</text>
				</view>
				<view class="item">
					<view class="head">
						<view class="info">
							<view class="icon">
								<image src="../../static/node_icon_node_white.png" mode=""></image>
							</view>
							<view class="name">
								<view class="text">Syq6reqeqiozxichaops123zSyq6reqeqiozxichaops123z</view>
								<view class="note">IP:52.82.101.206:9069</view>
							</view>
						</view>
						<view class="del">
							<image src="../../static/icon_close_white.png" mode=""></image>
						</view>
					</view>
					<view class="item-select">
						<view class="select">
							选择
						</view>
					</view>
				</view>
				<view class="item used">
					<view class="head">
						<view class="info">
							<view class="icon">
								<image src="../../static/node_icon_node_white.png" mode=""></image>
							</view>
							<view class="name">
								<view class="text">Syq6reqeqiozxichaops123zSyq6reqeqiozxichaops123z</view>
								<view class="note">IP:52.82.101.206:9069</view>
							</view>
						</view>
						<view class="del">
							<image src="../../static/icon_close_white.png" mode=""></image>
						</view>
					</view>
					<view class="item-select">
						<view class="text-used">
							已使用
						</view>
					</view>
				</view>
				<view class="item">
					<view class="head">
						<view class="info">
							<view class="icon">
								<image src="../../static/node_icon_node_white.png" mode=""></image>
							</view>
							<view class="name">
								<view class="text">Syq6reqeqiozxichaops123z</view>
								<view class="note">IP:52.82.101.206:9069</view>
							</view>
						</view>
						<view class="del">
							<image src="../../static/icon_close_white.png" mode=""></image>
						</view>
					</view>
					<view class="item-select">
						<view class="select">
							选择
						</view>
					</view>
				</view>
				
			</view>
		</uni-popup>
	</view>
	
</template>

<script>
	import uniPopup from '@/components/uni-popup.vue'
	export default {
		components: {
			uniPopup
		},
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
			popupShow(val){
				this.$refs[val].open()
			},
			popupHide(val){
				this.$refs[val].close()
			},
			activation(){
				uni.showToast({
				    title: '激活成功',
					icon:'success'
				});
			}
		}
	}
</script>

<style lang="less">
	.masterNodeCreate {
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

				.select {
					width: 124rpx;
					height: 46rpx;
					background-color: #1abb9b;
					border-radius: 23rpx;
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
		position: absolute;
		left: 0;
		bottom: 0;
		width: 100%;
		height: 97rpx;
		display: flex;
		flex-direction: row;
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
		.goRegister {
			height: 97rpx;
			flex: 1;
			line-height: 97rpx;
			text-align: center;
			color: #1abb9b;
		}
	}
	.popup-bottom{
		height: 960rpx;
		width: 100%;
		background: #FFFFFF;
		border-radius: 50rpx 50rpx 0 0;
		padding-top: 35rpx;
		.title{
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 0 40rpx;
			.name{
				font-size: 36rpx;
				color: #333333;
			}
			.cancel{
				font-size: 26rpx;
				color: #999999;
			}
		}
		.item{
			width: 702rpx;
			// height: 179rpx;
			background-color: #1abb9b;
			border-radius: 30rpx;
			margin: 0 auto;
			font-size: 26rpx;
			color: #FFFFFF;
			padding:30rpx;
			margin-top: 40rpx;
			.head{
				display: flex;
				justify-content: space-between;
				// align-items: center;
				// padding-top: 30rpx;
				.info{
					display: flex;
					// justify-content: space-between;
					align-items: center;
					.icon{
						width: 70rpx;
						height: 70rpx;
						// background-color: rgba(255, 255, 255, 0.2);
						// border-radius: 14rpx;
						// display: flex;
						// align-items: center;
						// justify-content: center;
						image{
							width: 100%;
							height: 100%;
						}
					}
					.name{
						margin-left: 20rpx;
						.text{
							width: 400rpx;
							overflow: hidden;
							text-overflow:ellipsis;
							white-space: nowrap;
						}
						.note{
							
						}
					}
				}
				.del{
					width: 40rpx;
					height: 40rpx;
					display: flex;
					align-items: center;
					justify-content: center;
					image{
						width: 24rpx;
						height: 24rpx;
					}
				}
			}
			.item-select{
				display: flex;
				flex-direction: row-reverse;
				.select{
					width: 161rpx;
					height: 46rpx;
					background-color: #f8f8f8;
					border-radius: 23rpx;
					// float: right;
					color: #1abb9b;
					line-height: 46rpx;
					text-align: center;
				}
				.text-used{
					height: 46rpx;
				}
			}
		}
		.used{
			background-color: rgba(26, 187, 155, 0.35);
		}
		.rescanBtn {
			position: fixed;
			left: 0;
			bottom: 0;
			width: 100%;
			height: 97rpx;
			font-size: 26rpx;
		
			.Btn {
				width: 469rpx;
				height: 97rpx;
				background-color: #1abb9b;
				border-radius: 0rpx 60rpx 0rpx 0rpx;
				color: #FFFFFF;
				display: flex;
				justify-content: center;
				align-items: center;
				image{
					height: 27rpx;
					width: 27rpx;
				}
				text{
					margin-left: 20rpx;
				}
			}
		}
	}
</style>
