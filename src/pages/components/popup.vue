<template>
	<view>
		<view class="mask"></view>
		
			<view class="redbox">
				<image src="https://www.baibianlg.com/xcx/index_dialog.png"></image>
				<view class="wrapBox">
					<view class="tips">
						<view>恭喜您注册成功</view>
						<view style="padding-top:10upx">获得新人礼包</view>
					</view>
					<view class="money">￥<text>{{money}}</text></view>
					<view class="btn" @click="eventClick">收下礼包</view>
				</view>
				<view class="close" @click="close"><icon type="clear" size="30" color="#fff"/></view>
			</view>
		
		
		
	</view>
</template>

<script>
	
	export default {
		props: {
			type: {
				type: String,
				default:'1'
			},
			title:{
				type:String,
				default:''
			},
			money:{
				type:Number,
				default:1
			},
			content:{
				type:String,
				default:''
			},
			version:{
				type:String,
				default:''
			}
		},
		data() {
			return {};
		},
		methods:{
			close(){
				this.$emit('close');
			},
			eventClick(){
				this.$emit('eventClick');
			}
		}
	}
</script>

<style lang="less">
	.mask{
		position: fixed;
		top: 0;
		left:0;
		width: 100%;
		height: 100%;
		z-index:1100;
		background-color: rgba(0, 0, 0, 0.6);
	}
	.btn{
		width:70%;
		margin:20rpx auto;
		margin-top:40rpx;
		padding:20rpx 0px;
		text-align:center;
		background:#4884FF;
		border-radius: 34px;
		font-size: 30rpx;
		color:#fff;
	}
	//微信弹窗
	.wxbox{
		position: absolute;
		top:20%;
		z-index: 998;
		width:80%;
		left:10%;
		background-color: #fff;
		border-radius:30rpx;
		padding:30rpx 0rpx;
		.close{
			position: absolute;
			top:5px;
			right:10px;
			z-index: 999;
			text-align: center;
		}
		.weixin{
			margin:20px 0 0 0px;
			text-align: center;
			image{
				width:100px;
				height:100px;
			}
		}
		.tips{
			padding:10rpx 20rpx;
			text-align:center;
			font-size:35rpx;
			color:#333;
		}
	}
	//红包弹窗
	.redbox{
		position: absolute;
		top:20%;
		z-index: 1200;
		width:90%;
		left:5%;
		padding:10rpx 0rpx;
		height:750rpx;
		image{
			width:100%;
			height:100%;
		}
		.close{
			text-align: center;
		}
		.wrapBox{
			position: absolute;
			width:60%;
			left:20%;
			top:320rpx;
			padding:10rpx 0rpx;
			text-align:center;
			.tips{
				font-size:35rpx;
				color:#fff;
				font-weight:bold;
				text{
					font-weight: normal;
				}
			}
			.money{
				font-size: 35rpx;
				color:#fff;
				margin-top:30rpx;
				font-weight: bold;
				text{
					font-size: 50rpx;
				}
			}
			.btn{
				width:80%;
				margin:20rpx auto;
				margin-top:40rpx;
				padding:20rpx 0px;
				text-align:center;
				background:linear-gradient(to bottom,#FFF04D,#FFE06B);
				border-radius: 34px;
				font-size: 30rpx;
				color:#CF2A2A;
				font-weight: bold;
			}
		}
	}
	.messBox{
		position: absolute;
		top:12%;
		z-index:998;
		width:80%;
		left:10%;
		padding:10rpx 0rpx;
		.wrapBox{
			background-color: #fff;
			border-radius: 20rpx;
			padding:30rpx;
			.title{
				text-align:center;
				font-size: 32rpx;
				font-weight: bold;
			}
			.desc{
				height:400rpx;
				margin-top:20rpx;
				font-size: 30rpx;
			}
		}
	}
	.updateBox{
		position: absolute;
		top:20%;
		z-index:998;
		height:300rpx;
		width:80%;
		left:10%;
		.tubiao{
			text-align: center;
			image{
				z-index: 999;
				width:200rpx;
				height:130rpx;
			}
		}
		.wrapbox{
			position: relative;
			z-index: 998;
			top:-70rpx;
			background-color: #fff;
			border-radius: 10rpx;
			padding:30rpx 40rpx;
			.version{
				margin-top:50rpx;
				font-size: 35rpx;
				color:#333;
				font-weight: bold;
				text-align: center;
			}
			.desc-t{
				margin-top:30rpx;
				font-size: 32rpx;
				font-weight: bold;
			}
		}
	}
	.updateBox1{
		position: absolute;
		top:15%;
		z-index:998;
		width:80%;
		left:10%;
		padding:10rpx;
		height:700rpx;
		image{
			width:100%;
			height:100%;
		}
		.wrapBox{
			position: absolute;
			width:85%;
			left:50rpx;
			top:40rpx;
			padding:10rpx 20rpx;
			.version{
				font-size: 35rpx;
				color:#fff;
			}
			.desc-t{
				margin-top:100rpx;
				font-size: 32rpx;
				font-weight: bold;
			}
		}
	}
	.desc{
		height:230rpx;
		overflow:scroll;
		margin-top:10rpx;
		font-size: 30rpx;
		color:#666;
		line-height:50rpx;
	}
	.btnbox{
		display: flex;
		justify-content: space-around;
		margin:40rpx 0rpx 20rpx 0rpx;
		margin-top:50rpx;
		.btnno{
			padding:10rpx 30rpx;
			background-color: #f8f8f8;
			border-radius: 10rpx;
			font-size: 30rpx;
			color:#666;
		}
		.btnUp{
			padding:10rpx 30rpx;
			background-color: #4884FF;
			border-radius: 10rpx;
			font-size: 30rpx;
			color:#fff;
		}
	}
</style>
