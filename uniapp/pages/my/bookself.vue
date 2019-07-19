<template>
	<div class='wrapper'>
		<div class='header'>
			<image class="pre" src="../../static/images/nextyear.png" mode=""></image>
			<text class="text">2019年</text>
			<image class="next" src="../../static/images/nextyear.png" mode=""></image>
		</div>
		<div class='month'>
			<div class='month-detail'>7月</div>
			<div class='count'>共23本</div>
		</div>
		<view class="book-wrapper">
			<image class="book-img" src="../../static/images/book-iocn2.png" mode=""></image>
			<view class="book-content">
				<text class="title">笠翁对韵</text>
				<text class="desc">作家榜经典：笠翁对韵+笠翁对韵+识字神器套装 &#913-6岁]</text>
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
				<text class="desc">作家榜经典：笠翁对韵+笠翁对韵+识字神器套装 &#913-6岁]</text>
				<view class="author">
					<view class="book-desc">
						<image class="img-icon" src="../../static/images/author-icon.png" mode=""></image>
						<text class="name">朝花夕拾</text>
					</view>
					<text class="seecount">567人浏览</text>
				</view>
			</view>
		</view>
		
		<div class='month'>
			<div class='month-detail'>8月</div>
			<div class='count'>共23本</div>
		</div>
		<view class="book-wrapper">
			<image class="book-img" src="../../static/images/book-iocn2.png" mode=""></image>
			<view class="book-content">
				<text class="title">笠翁对韵</text>
				<text class="desc">作家榜经典：笠翁对韵+笠翁对韵+识字神器套装 &#913-6岁]</text>
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
				<text class="desc">作家榜经典：笠翁对韵+笠翁对韵+识字神器套装 &#913-6岁]</text>
				<view class="author">
					<view class="book-desc">
						<image class="img-icon" src="../../static/images/author-icon.png" mode=""></image>
						<text class="name">朝花夕拾</text>
					</view>
					<text class="seecount">567人浏览</text>
				</view>
			</view>
		</view>
	</div>
</template>

<script>

</script>

<style lang="scss" scoped>
	.wrapper {
		min-height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		background-color: #f5f5f5;
		padding: 32upx 0;
		padding-bottom: 122upx;
		.header {
			width: 686upx;
			height: 72upx;
			border-radius: 36upx;
			margin-left: 32upx;
			padding: 0 32upx;
			box-sizing: border-box;
			display: flex;
			justify-content: space-between;
			align-items: center;
			background-color: #fff;

			image {
				height: 24upx;
				width: 11upx;
			}

			text {
				font-size: 28upx;
				font-family: PingFangSC-Medium;
				font-weight: 500;
				color: rgba(34, 34, 34, 1);
			}

			.next {
				transform: rotate(180deg)
			}
		}

		.month {
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 32upx;
			.month-detail {
				font-size: 28upx;
				font-family: PingFangSC-Medium;
				font-weight: 500;
				color: rgba(34, 34, 34, 1);
			}

			.count {
				font-size: 28upx;
				font-family: PingFangSC-Regular;
				font-weight: 400;
				color: rgba(102, 102, 102, 1);
			}
		}
		.book-wrapper {
			display: flex;
			background-color: #fff;
			padding: 32upx;
			box-sizing: border-box;
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
</style>
