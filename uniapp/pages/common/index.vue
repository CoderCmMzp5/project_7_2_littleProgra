<template>
	<div class='content'>
		<image class="bg" src="../../static/images/home_bg.png" mode="widthFix"></image>
		<view class="icon-1">
			<image class="icon-img" src="https://r.ffimg.cn/hlswx/2019-07-04/5d1dfc033eac8824854881.png" mode="widthFix"></image>
			<text class="count">2/5</text>
			
		</view>
		<view class="same-icon">
			<image class="img-icon" src="../../static/images/home_icon2.png" mode=""></image>
			<text class="desc">读书城堡</text>
			<image class="img-icon-small" src="../../static/images/icon2.png" mode=""></image>
		</view>
		<view class="same-icon" @click="_goToPictureBook">
			<image class="img-icon" src="../../static/images/home_icon3.png" mode=""></image>
			<text class="desc">绘本试读</text>
			<image class="img-icon-small" src="../../static/images/icon3.png" mode=""></image>
		</view>
		<view class="same-icon" @click="_goToReadingPromotion">
			<image class="img-icon" src="../../static/images/home_icon4.png" mode=""></image>
			<text class="desc">阅读推广</text>
			<image class="img-icon-small" src="../../static/images/icon4.png" mode=""></image>
		</view>
		<view class="read-wrapper">
			<view class="head-content">
				<text class="title">推荐阅读</text>
				<text class="border"></text>
			</view>
			<view class="book-wrapper"  @click="_goToRead">
				<image class="book-img" src="../../static/images/book-iocn1.png" mode=""></image>
				<view class="book-content">
					<text class="title">笠翁对韵</text>
					<text class="desc">作家榜经典：笠翁对韵+识字神器套装 &#913-6岁]</text>
					<view class="author">
						<view class="book-desc">
							<image class="img-icon" src="../../static/images/author-icon.png" mode=""></image>
							<text class="name">朝花夕拾</text>
						</view>
						<text class="seecount">567人浏览</text>
					</view>
				</view>
			</view>
			
			<view class="book-wrapper">
				<image class="book-img" src="../../static/images/book-iocn2.png" mode=""></image>
				<view class="book-content">
					<text class="title">笠翁对韵</text>
					<text class="desc">作家榜经典：笠翁对韵+识字神器套装 &#913-6岁]</text>
					<view class="author">
						<view class="book-desc">
							<image class="img-icon" src="../../static/images/author-icon.png" mode=""></image>
							<text class="name">朝花夕拾</text>
						</view>
						<text class="seecount">567人浏览</text>
					</view>
				</view>
			</view>
		</view>
	</div>
</template>

<script>
	import { PAGE_PICTURE_BOOK, PAGE_READING_PROMOTION, PAGE_READ_BOOK } from '../../static/page-path.js'
	 export default {
        data(){
            return {
 
            }
        },
        onLoad(){
 
        },
        methods:{
			/* 
			* 	去绘本试读页面 
			*  */
            _goToPictureBook(){
				uni.navigateTo({
					url:PAGE_PICTURE_BOOK
				})
			},
			/* 
			* 去阅读推广页面
			*  */
			_goToReadingPromotion(){
				uni.navigateTo({
					url:PAGE_READING_PROMOTION
				})
			},
			//去阅读页面
			_goToRead(){
				uni.navigateTo({
					url:PAGE_READ_BOOK
				})
			}
        }
    }
</script>

<style lang="scss" scoped>
	.content {
		padding: 0 32upx;
		height: auto;
		font-family: PingFangSC-Semibold;
		.bg {
			position: absolute;
			top: 0;
			left: 0;
			height: 200upx;
			width: 100%;
			z-index: -1;
		}

		.icon-1 {
			margin: 0upx 0 30upx 0;
			height: 360upx;
			width: 100%;
			position: relative;
			.icon-img{
				height: 100%;
				width: 100%;
				position: absolute;
				z-index: 10;
			}
			.count{
				position: absolute;
				right: 32upx;
				bottom: 32upx;
				background:#222;
				opacity: 0.5;
				border-radius:16px;
				height: 32upx;
				width: 64upx;
				display: flex;
				justify-content: center;
				align-items: center;
				color: #fff;
				font-size: 18upx;
				font-family:PingFangSC-Regular;
				font-weight:400;
				z-index: 1000;
			}
		}

		.same-icon {
			height: 200upx;
			width: 100%;
			position: relative;
			margin-bottom: 24upx;

			.img-icon {
				height: 100%;
				width: 100%;
			}

			.desc {
				position: absolute;
				z-index: 100;
				top: 72upx;
				left: 48upx;
				font-weight: 600;
				color: #fff;
				font-size: 40upx;
			}

			.img-icon-small {
				height: 100upx;
				width: 100upx;
				position: absolute;
				;
				z-index: 100;
				top: 50upx;
				right: 24upx;
			}
		}

		.read-wrapper {
			.head-content {
				display: flex;
				margin-top: 40upx;
				position: relative;

				.title {
					font-size: 40upx;
					color: #222;
					font-weight: 500;
					font-family: PingFangSC-Medium;
				}

				.border {
					height: 16upx;
					width: 160upx;
					background-color: #f2cb2c;
					position: absolute;
					left: 0;
					top: 40upx;
					z-index: -1;
				}
			}

			.book-wrapper {
				display: flex;
				margin-top: 40upx;
				.book-img {
					flex: 0 0 200upx;
					height: 200upx;
					margin-right: 24upx;
				}

				.book-content {
					display: flex;
					flex-direction: column;
					justify-content: space-between;

					.title {
						font-size: 28upx;
						color: #222;
						font-family: PingFangSC-Medium;
						font-weight: 500;
						color: rgba(34, 34, 34, 1);
					}
					.desc{
						margin-top: 24upx;
						font-size: 24upx;
						font-family:PingFangSC-Regular;
						font-weight:400;
						color:rgba(102,102,102,1);
					}
					.author{
						display: flex;
						justify-content: space-between;
						font-family: PingFangSC-Regular;
						font-size: 24upx;
						margin-top:34upx ;
						.book-desc{
							display: flex;
							align-items: center;
							color: #222;
							font-weight: 400;
							.img-icon{
								height: 40upx;
								width: 40upx;
								margin-right: 16upx;
							}
							.name{
								color: #222;
								font-size: 24upx;
								font-family:PingFangSC-Regular;
								font-weight:400;
							}
						}
						.seecount{
							color: #999;
						}
					}
				}
			}
		}
	}
</style>
