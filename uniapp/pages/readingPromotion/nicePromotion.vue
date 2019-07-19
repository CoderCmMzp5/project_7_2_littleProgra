<template>
	<view class="wrapper">
		<view class="block">	
		</view>
		<view class="header">
			<text class="title">推荐书籍</text>
			<view class="support-content">
				<image class="head-img" src="../../static/images/book-img.png" mode=""></image>
				<view class="desc">
					<image src="../../static/images/dot-icon.png" class="icon" mode=""></image>
					<text class="title">闲适的时光</text>
					<text class="author">人民出版社</text>
				</view>
				<view class="listen-icon">
					<image src="../../static/images/listen_icon.png" mode=""></image>
					<text>听书</text>
				</view>
			</view>
		</view>
		<view class="block"></view>
		<view class="reson-content">
			<text class="title">推荐作者</text>
			<input type="text" placeholder="在此输入您的推荐作者" style="margin-top: 32upx;" placeholder-style='color: #bbb; font-size: 14px;'>
		</view>
		<view class="block"></view>
		<view class="reson-content">
			<text class="title">推荐理由</text>
			<textarea value=""  maxlength="300" placeholder="在此输入您的推荐理由" placeholder-style='color: #bbb; font-size: 14px;'  class="textarea"/>
			<view class="number">
				<text>0/300</text>
			</view>
		</view>
		<view class="reason-img">
			<view class="img-content">
				<image src="../../static/images/detail-icon3.png" mode="" class="imgdetail"></image>
				<image src="../../static/images/close_icon.png" mode="" class="close"></image>
			</view>
			<view class="img-content">
				<image src="../../static/images/detail-icon4.png" mode="" class="imgdetail"></image>
				<image src="../../static/images/close_icon.png" mode="" class="close"></image>
			</view>
			<view class="img-content">
				<image src="../../static/images/add_icon.png" mode="" class="imgdetail"></image>
			</view>
		</view>
		<button  class="btn">提交</button>
	</view>
	
</template>

<script>
</script>

<style scoped lang="scss">
	.wrapper{
		.block{
			height: 32upx;
			width: 100%;
			background-color: #f5f5f5;
		}
		height: 100%;
		width: 100%;
		.header{
			padding: 32upx;
			box-sizing: border-box;
			background-color: #fff;
			.title{
				font-size: 28upx;
				color: #222;
			}
			.support-content{
				display: flex;
				margin-top: 32upx;
				position: relative;
				.listen-icon {
					position: absolute;
					top: 0;
					right: 0;
					display: flex;
					align-items: center;
				
					image {
						width: 30upx;
						height: 26upx;
						margin-right: 15upx;
					}
						
					text {
						font-size: 28upx;
						font-family: PingFangSC-Regular;
						font-weight: 400;
						color: rgba(241, 187, 0, 1);
					}
				}
				.head-img{
					flex: 0 0 153upx;
					height: 200upx;
				}
				.desc{
					display: flex;
					flex-direction: column;
					justify-content: space-between;
					margin-left: 38upx;
					.icon{
						height: 36upx;
						width: 40upx;
					}
					.title{
						font-size: 48upx;
						color: #222222;
						font-family:PingFangSC-Medium;
						font-weight:500;
						margin-top: 44upx;
					}
					.author{
						margin-top: 8upx;
						font-size: 24upx;
						font-family:PingFangSC-Regular;
						font-weight:400;
					}
				}
			}
		}
		.reson-content{
			padding: 32upx;
			.title{
				color: #222;
				font-size: 28upx;
				font-weight: 500;
			}
			.textarea{
				margin-top: 32upx;
				height: 112upx;
				width: 100%;
				font-size: 24upx;
				color: #666;
				
			}
			.number{
				display: flex;
				justify-content: flex-end;
				font-size: 18upx;
				color: #bbb;
			}
		}
		.reason-img{
			display: flex;
			justify-content: space-between;
			margin-top: 30upx;
			padding: 0 32upx;
			box-sizing: border-box;
			.img-content{
				flex: 0 0 202upx;
				height: 202upx;
				position: relative;
				.imgdetail{
					height: 100%;
					width: 100%;
				}
				.close{
					position: absolute;
					top:0;
					right: 0;
					height: 32upx;
					width: 32upx;
				}
				.add{
					font-size: 40upx;
				}
				
			}
		}
		.btn{
			width: 686upx;
			height: 94upx;
			line-height: 94upx;
			background:linear-gradient(225deg,rgba(247,234,122,1) 0%,rgba(241,187,0,1) 100%);
			color: #222;
			font-size: 28upx;
			box-shadow:0px 10px 30px 0px rgba(247,231,115,0.5);
			border-radius: 16upx;
			margin-top: 64upx;
		}
		button::after{
			border:  none
		}
	}
</style>
