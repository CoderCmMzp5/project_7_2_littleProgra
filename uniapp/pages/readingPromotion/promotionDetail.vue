<template>
	<div class='wrapper'>
		<view class="content">
			<view class="header">
				<image class="head-img" src="../../static/images/book-img.png" mode=""></image>
				<view class="desc">
					<image class="img-icon" src="../../static/images/dot-icon.png" mode=""></image>
					<text class="title">闲适的时光</text>
					<text class="author">人民出版社</text>
				</view>
			</view>
			<view class="middle">
				<view class="head-content">
					<text class="title">推荐人</text>
					<text class="border"></text>
				</view>
				<view class="name">
					<image src="../../static/images/author-icon.png" class="book-author-img" mode=""></image>
					<text class="book-name">清明雨上</text>
				</view>
				
				<view class="head-content-reason">
					<text class="title">推荐理由</text>
					<text class="border"></text>
				</view>
				<text class="support-reason">
					清醒隽永是不必说了。吸引我看下去的，不仅是因为作者讲了一个关于“不死”的故事，还因为作者在开头几章抛出了许多待解的细节，却一点儿也不急着告诉你答案，你就知道里面会有些好东西。不是所有人都能得到的好东西，因为它要求你沉得住气。
				</text>
				<view class="suppprt-img">
					<image src="../../static/images/book-img.png" mode=""></image>
					<image src="../../static/images/book-img.png" mode=""></image>
					<image src="../../static/images/book-img.png" mode=""></image>
				</view>
				<view class="dot">
					<view class="dot-content">
						<image src="../../static/images/zan_icon.png" mode="" class="icon"></image>
						<text class="text">1346</text>
					</view>
					<view class="dot-content">
						<image src="../../static/images/share_icon.png" mode=""class="icon"></image>
						<text class="text">分享</text>
					</view>
				</view>
			</view>
		</view>
		<view class="roule">
			<text class="title">活动规则</text>
			<text class="desc">1、坚持阅读，每坚持七天阅读会自动发放一张补签卡至您的账户</text>
		</view>
	</div>
</template>

<script>
	
</script>	

<style scoped lang="scss">
	.wrapper{
		height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		padding: 32upx;
		box-sizing: border-box;
		.content{
			padding: 32upx;
			background-color: #FFFFFF;
			border-radius:16px;
			box-sizing: border-box;
			.header{
				display: flex;
				.head-img{
					flex: 0 0 153upx;
					height: 200upx;
				}
				.desc{
					display: flex;
					flex-direction: column;
					justify-content: space-between;
					margin-left: 38upx;
					.img-icon{
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
			.middle{
				margin-top: 40upx;
				display: flex;
				flex-direction: column;
				.head-content, .head-content-reason {
					display: flex;
					position: relative;
					height: 28upx;
					width: 100%;
					.title {
						font-size: 28upx;
						color: #222;
						font-weight: 500;
						font-family: PingFangSC-Medium;
						position: absolute;
						top: 0;
						z-index: 100;
					}
				
					.border {
						height: 16upx;
						width: 84upx;
						background-color: #f2cb2c;
						position: absolute;
						left: 0;
						top: 25upx;
						z-index: 10;
					}
				}
				.head-content-reason{
					margin-top: 40upx;
					.border{
						width: 112upx;
						
					}
				}
				.support-reason{
					margin-top: 22upx;
					margin-bottom: 20upx;
					font-size: 24upx;
					font-family:PingFangSC-Regular;
					font-weight:400;
					color:rgba(34,34,34,1);
				}
				.suppprt-img{
					display: flex;
					justify-content: space-between;
					align-items: center;
					image{
						height: 202upx;
						flex: 0 0 202upx;
					}
				}
				.dot{
					display: flex;
					align-items: center;
					margin-top: 32upx;
					.dot-content{
						display: flex;
						align-items: center;
						.icon{
							height: 36upx;
							width: 36upx;
							margin-right: 13upx;
						}
						.text{
							color: #999;
							font-size: 24upx;
						}
					}
					.dot-content:nth-of-type(2){
						margin-left: 64upx;
					}
					
				}
				.name{
					display: flex;
					align-items: center;
					margin-top: 30upx;
					.book-author-img{
						height: 80upx;
						flex: 0 0 80upx;
						border-radius: 50%;
					}
					.book-name{
						color: #222222;
						font-size: 28upx;
						margin-left: 16upx;
					}
				}
			}
		}
		.roule{
			margin-top: 32upx;
			display: flex;
			flex-direction: column;
			padding: 0 32upx;
			.title{
				color: #666;
				font-size: 24upx;
				font-weight: 500;
			}
			.desc{
				margin-top: 16upx;
				font-size: 24upx;
				color: #999;
			}
		}
	}
</style>
