<template>
	<div class='wrapper'>
		<view class="question">
			<view class="title">
				<text class="current">4</text>
				<text class="total">/共16题</text>
			</view>
			<view class="desc">
				以下的几位诗人中是唐代诗人的是？
			</view>
			<view class="select">
				<view class="select-item">
					<text class="text">A.李白</text>
					<text class="radius"></text>
				</view>
				<view class="select-item">
					<text class="text error">B.李白</text>
					<image class="img-icon" src="../../static/images/error.png" mode=""></image>
				</view>
				<view class="select-item">
					<text class="text">C.李白</text>
					<text class="radius"></text>
				</view>
				<view class="select-item">
					<text class="text right">D.以上几位都是</text>
					<image class="img-icon" src="../../static/images/right.png" mode=""></image>
				</view>
			</view>
			<button type="primary" class="btn" @click="_goToAnswerQuestion">下一题</button>
		</view>
	</div>
</template>

<script>
</script>

<style scoped lang="scss">
	.wrapper{
		min-height: 100%;
		width: 100%;
		padding: 32upx;
		box-sizing: border-box;
		background-color: #f5f5f5;
		.question{
			margin-top: 32upx;
			border-radius: 16upx;
			background-color: #fff;
			padding: 32upx;
			padding-bottom: 64upx;
			box-sizing: border-box;
			.title{
				display: flex;
				align-items: flex-end;
				image{
					height: 45upx;
					width: 45upx;
					margin-right: 16upx;
				}
				.current{
					position: relative;
					top: 10upx;
				}
				.current, .total{
					color: #999;
					font-size: 56upx;
					font-family:PingFangSC-Medium;
				}
				.total{
					font-size: 24upx;
				}
			}
			.desc{
				color: #222;
				font-size: 40upx;
				font-family: PingFangSC-Medium;
				font-weight: 500;
				margin-top: 16upx;
			}
			.select{
				display: flex;
				flex-direction: column;
				margin-top: 9upx;
				.select-item{
					display: flex;
					align-items: center;
					justify-content: space-between;
					height: 104upx;
					.text{
						font-size: 28upx;
						color: #222;
						font-weight: 500;
						font-family:PingFangSC-Medium;
					}
					.radius{
						height: 36upx;
						width: 36upx;
						border-radius: 50%;
						border: 1upx solid #ccc;
					}
					.error{
						color: #F5222D;
					}
					.right{
						color: #F2CB2C;
					}
					.img-icon{
						height: 36upx;
						width: 36upx;
					}
				}
			}
			.btn{
				margin-top: 32upx;
				height: 94upx;
				width: 100%;
				line-height: 94upx;
				border-radius: 16upx;
				background:linear-gradient(225deg,rgba(247,234,122,1) 0%,rgba(241,187,0,1) 100%);
				box-shadow:0px 10px 30px 0px rgba(247,231,115,0.5);
				font-size: 28upx;
				color: #222;
				font-family: PingFangSC-Medium;
				font-weight: 500;
			}
			button::after{
				border: none
			}
		}
	}
</style>
