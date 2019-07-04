<template>
	<div class='wrapper'>
		<view class="content">
			<image src="https://r.ffimg.cn/hlswx/2019-07-04/5d1dfcf2c1391210088269.png" class="bg"></image>
			<view class="content-detail">
				<view class="my-level">
					<text class="text">我的等级</text>
					<view class="share">
						<image class="share-icon" src="../../static/images/share_icon.png" mode=""></image>
						<text class="text">分享</text>
					</view>
				</view>
				<image src="../../static/images/author-icon.png" mode="" class="img-icon"></image>
				<view class="title">
					当前等级: 书虫
				</view>
				<view class="progress">
					<text class="name">书虫</text>
					<progress class="progress-width" percent="40" activeColor='#FFE500' backgroundColor="#F4F4F4" active stroke-width="5" />
					<text class="desc">书虫</text>
				</view>
				<view class="distance">距离获得书霸称号还需打卡20天</view>
			</view>
		</view>
		<view class="book-interest">
			<text class="title">当前等级特权</text>
			<text class="common">免费阅读书籍：20本</text>
			<text class="common">免费阅读绘本：10本</text>
			<text class="common">免费听书：5本</text>
		</view>
	</div>
</template>

<script>
</script>

<style lang="scss" scoped>
	.wrapper{
		min-height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		padding: 32upx 0;
		box-sizing: border-box;
		.content{
			height: 721upx;
			width: 100%;
			position: relative;
			.bg{
				height: 100%;
				width: 100%;
				position: absolute;
				z-index: 10;
			}
			.content-detail{
				height: 100%;
				width: 100%;
				padding: 32upx 64upx;
				box-sizing: border-box;
				position: absolute;
				z-index: 100;
				.my-level{
					display: flex;
					justify-content: space-between;
					padding-top: 15upx;
					.text{
						color: #222;
						font-size: 30upx;
					}
					.share{
						display: flex;
						align-items: center;
						.share-icon{
							height: 36upx;
							width: 36upx;
						}
						.text{
							color: #999;
							font-size: 26upx;
							margin-left: 13upx;
						}
					}
				}
				.img-icon{
					height: 200upx;
					width: 200upx;
					margin-left: 200upx;
					margin-top: 92upx;
				}
				.title{
					text-align: center;
					margin-top: 60upx;
					font-size: 30upx;
					color: #222;
				}
				.progress{
					display: flex;
					justify-content: space-between;
					margin-top: 68upx;
					.name, .desc{
						flex: 0 0 68upx;
						font-size: 18upx;
						display: flex;
						justify-content: center;
						align-items: center;
						border-radius: 16upx;
					}
					.name{
						background: linear-gradient(270deg,rgba(250,231,87,1) 0%,rgba(242,203,44,1) 100%);
						color: #FF4B00;
					}
					.desc{
						background: linear-gradient(90deg,rgba(198,198,198,1) 0%,rgba(221,221,221,1) 100%);;
						color: #fff;
					}
					.progress-width{
						flex: 1;
						margin: 0 11upx;
					}
				}
				.distance{
					width: 100%;
					text-align: center;
					margin-top: 30upx;
					font-size: 26upx;
					color: #999;
				}
			}
			
		} 
		.book-interest{
			display: flex;
			flex-direction: column;
			margin: 32upx;
			padding:0 32upx 32upx 32upx;;
			box-sizing: border-box;
			background-color: #fff;
			justify-content: space-between;
			align-items: flex-start;
			border-radius: 16upx;
			.title{
				font-size: 30upx;
				color: #222;
				font-weight: 500;
				margin-top: 32upx;
			}
			.common{
				font-size: 26upx;
				color: #222;
				margin-top: 32upx;
			}
		}
	}
</style>
