<template>
	<view class="wrapper">
		<view class="content">
			<image class="book-img" src="../../static/images/book-iocn1.png" mode=""></image>
			<text class="name">闲适的时光</text>
			<text class="author">人民出版社</text>
			<view class="player">
				<image class="player-img" src="../../static/images/player.png" mode=""></image>
				<image class="player-img" src="../../static/images/player-1.png" mode=""></image>
				<image class="player-img" src="../../static/images/player.png" mode=""></image>
			</view>
			<view class="progress">
				<progress class="progress-width" percent="40" activeColor='#FFE500' backgroundColor="#F4F4F4" active stroke-width="5" />
				<view class="time">
					<text class="start">01:12</text>
					<text class="end">04:43</text>
				</view>
			</view>
		</view>
		
		<view class="question">
			<view class="title">
				<image src="../../static/images/question-icon.png" mode=""></image>
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
	</view>
</template>

<script>
	import { PAGE_ANSWER_QUESTION } from '../../static/page-path.js'
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			_goToAnswerQuestion(){
				uni.navigateTo({
					url:PAGE_ANSWER_QUESTION
				})
			}
		}
	}
	
</script>

<style lang="scss" scoped>
	.wrapper{
		min-height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		padding: 32upx;
		box-sizing: border-box;
		.content{
			display: flex;
			justify-content: center;
			align-items: center;
			flex-direction: column;
			padding: 32upx;
			padding-top: 40upx;
			box-sizing: border-box;
			background-color: #fff;
			border-radius: 16upx;
			.book-img{
				height: 416upx;
				width: 320upx;
			}
			.name{
				margin-top: 32upx;
				color: #222;
				font-size: 48upx;
				font-weight: 500;
				font-family:PingFangSC-Medium;
			}
			.author{
				margin-top: 8upx;
				font-size: 24upx;
				color: #666;
				font-family:PingFangSC-Regular;
			}
			.player{
				width: 100%;
				margin-top: 32upx;
				display: flex;
				justify-content: space-between;
				align-items: center;
				box-sizing: border-box;
				padding:  0 123upx;
				.player-img{
					height: 48upx;
					width: 48upx;
				}
				.player-img:nth-of-type(1){
					transform: rotate(-180deg)
				}
				.player-img:nth-of-type(2){
					height: 88upx;
					width: 88upx;
				}
			}
			.progress{
				width: 100%;
				margin-top: 42upx;
				.time{
					display: flex;
					justify-content: space-between;
					align-items: center;
					margin-top: 16upx;
					.start, .end{
						color: #222;
						font-size: 24upx;
						font-family:PingFangSC-Regular;
					}
					.end{
						color: #999;
					}
				}
			}
			
		}
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
