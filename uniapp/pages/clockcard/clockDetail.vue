<template>
	<view class="wrapper">
		<view class="date">
			<calendar :date="date" range='true' :selected="selected" :disable-before="true" :start-date="'2019-7-1'" :end-date="'2019-12-31'"
			 @change="change" @to-click="toClick">
			</calendar>
			<button type="primary" class="btn">立即打卡</button>
			<div class="text">本月已打卡5天</div>
			<view class="block" style="height: 64upx;"></view>
		</view>
		<view class="buchong">
			<view class="book-wrapper">
				<image class="book-img" src="../../static/images/book-iocn1.png" mode=""></image>
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
			<button type="primary" class="btn-1">使用补签卡</button>
		</view>
		<view class="desc-1">
			<text class="title">如何获得补签卡?</text>
			<text class="common">1、坚持阅读，每坚持七天阅读会自动发放一张补签卡至您的账户</text>
			<text class="common">2、活动发放…</text>
		</view>
	</view>
</template>

<script>
	import calendar from "@/components/uni-calendar/uni-calendar"
	export default {
		components: {
			calendar
		},
		data() {
			return {
				date: '2019-7-1',
				selected: [{
					date: '2019-7-5',
				}, {
					date: '2019-7-2'
				}, {
					date: '2019-7-3'
				}, {
					date: '2019-7-4'
				},{
					date: '2019-7-10'
				},{
					date: '2019-7-11'
				},{
					date: '2019-7-09'
				},{
					date: '2019-7-07'
				},{
					date: '2019-7-08'
				},{
					date: '2019-7-13'
				},{
					date: '2019-7-12'
				}],
			};
		},
		methods: {
			change(e) {
				console.log(e);
			},
			toClick(e) {
				console.log(e);
			}
		}
	}
</script>

<style scoped lang="scss">
	.wrapper {
		min-height: 100%;
		width: 100%;
		padding: 32upx;
		box-sizing: border-box;
		background-color: #f5f5f5;
		padding-bottom: 30upx;

		.date {
			border-radius: 16upx;
			background-color: #fff;

			.btn {
				height: 94upx;
				width: 622upx;
				border-radius: 16upx;
				background: linear-gradient(225deg, rgba(247, 234, 122, 1) 0%, rgba(241, 187, 0, 1) 100%);
				box-shadow: 0px 10px 30px 0px rgba(247, 231, 115, 0.5);
				margin-top: 49upx;
				color: #222;
				font-size: 28upx;
				font-weight: 500;
				line-height: 94upx;
			}

			.text {
				margin-top: 32upx;
				font-size: 24upx;
				font-family: PingFangSC-Medium;
				font-weight: 500;
				color: rgba(102, 102, 102, 1);
				text-align: center
			}

			button::after {
				border: none;
			}
		}

		.buchong {
			display: flex;
			flex-direction: column;
			align-items: center;
			border-radius: 16upx;
			width: 100%;
			margin-top: 32upx;
			padding: 32upx;
			padding-bottom: 64upx;
			box-sizing: border-box;
			background-color: #fff;

			.book-wrapper {
				display: flex;
				width: 100%;

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

					.desc {
						margin-top: 24upx;
						font-size: 24upx;
						font-family: PingFangSC-Regular;
						font-weight: 400;
						color: rgba(102, 102, 102, 1);
					}

					.author {
						display: flex;
						justify-content: space-between;
						font-family: PingFangSC-Regular;
						font-size: 24upx;
						margin-top: 34upx;

						.book-desc {
							display: flex;
							align-items: center;
							color: #222;
							font-weight: 400;

							.img-icon {
								height: 40upx;
								width: 40upx;
								margin-right: 16upx;
							}

							.name {
								color: #222;
								font-size: 24upx;
								font-family: PingFangSC-Regular;
								font-weight: 400;
							}
						}

						.seecount {
							color: #999;
						}
					}
				}
			}

			.btn-1 {
				height: 94upx;
				width: 100%;
				line-height: 94upx;
				background: linear-gradient(225deg, rgba(247, 234, 122, 1) 0%, rgba(241, 187, 0, 1) 100%);
				box-shadow: 0px 10px 30px 0px rgba(247, 231, 115, 0.5);
				border-radius: 16upx;
				font-size: 28upx;
				font-family: PingFangSC-Medium;
				font-weight: 500;
				color: rgba(34, 34, 34, 1);
				margin-top: 40upx;
			}

			button::after {
				border: none;
			}

		}

		.desc-1 {
			padding: 32upx;
			box-sizing: border-box;
			display: flex;
			flex-direction: column;

			.title {
				color: #666;
				font-weight: 500;
				font-family: PingFangSC-Medium;
				font-size: 24upx;
			}

			.common {
				color: #999;
				font-size: 24upx;
				font-weight: 400;
				font-family: PingFangSC-Regular;
				margin-top: 16upx;
			}
		}
	}
</style>
