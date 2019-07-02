<template>
	<view class="wrapper">
		<view class="header">
			<image class="bg" src="../../static/images/home_bg.png" mode=""></image>
			<view class="content">
				<image class="headimg" src="../../static/images/author-icon.png" mode=""></image>
				<view class="title">
					<text class="name">清明雨上</text>
					<text class="idcard">书仙</text>
				</view>
				<view class="time">
					<text class="sendcard">打卡</text>
					<text class="day">36天</text>
				</view>
			</view>
		</view>
		<view class="item-list">
			<view class="item-list-content" @click="_goToMemberMessage">
				<image class="item-img" src="../../static/images/my-icon-1.png" mode=""></image>
				<text class="text">会员信息</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goToMemberCard">
				<image class="item-img" src="../../static/images/my-icon-2.png" mode=""></image>
				<text class="text">会员海报</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goToBookself">
				<image class="item-img" src="../../static/images/my-icon-3.png" mode=""></image>
				<text class="text">打卡书单</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goTomemberLevel" >
				<image class="item-img" src="../../static/images/my-icon-4.png" mode=""></image>
				<text class="text">晋级奖励</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content">
				<image class="item-img" src="../../static/images/my-icon-5.png" mode=""></image>
				<text class="text">月阅计划</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goToAboutMe">
				<image class="item-img" src="../../static/images/my-icon-6.png" mode=""></image>
				<text class="text">关于我们</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>
		</view>

	</view>


</template>

<script>
	import { PAGE_MEMBER_MESSAGE, PAGE_MEMBER_CARD ,PAGE_BOOKSELF, PAGE_MEMBER_LEVEL, PAGE_ABOUT_ME, PAGE_REGIESTER} from '../../static/page-path.js'
	export default {

		data() {
			return {

			}
		},
		onLoad() {

		},
		methods: {
			//去会员信息
			_goToMemberMessage(){
				uni.navigateTo({
					url: PAGE_REGIESTER
				})
			},
			//去会员海报页面
			_goToMemberCard(){
				uni.navigateTo({
					url:PAGE_MEMBER_CARD
				})
			},
			//去打卡书单页面
			_goToBookself(){
				uni.navigateTo({
					url:PAGE_BOOKSELF
				})
			},
			//去会员等级页面
			_goTomemberLevel(){
				uni.navigateTo({
					url: PAGE_MEMBER_LEVEL
				});
			},
			//去关于我们
			_goToAboutMe(){
				uni.navigateTo({
					url:PAGE_ABOUT_ME
				})
			},
		}
	}
</script>

<style lang="scss" scoped>
	.wrapper {
		height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		.header {
			position: relative;
			padding: 14upx 32upx 18upx 32upx;
			margin-bottom: 14upx;
			.bg {
				position: absolute;
				top: 0;
				left: 0;
				width: 100%;
				height: 224upx;
				z-index: 10;
			}

			.content {
				height: 192upx;
				width: 100%;
				display: flex;
				align-items: center;
				padding: 32upx;
				background-color: #FFFFFF;
				border-radius: 16upx;
				box-sizing: border-box;
				position: relative;
				z-index: 100;
				.headimg {
					flex: 0 0 128upx;
					height: 128upx;

				}

				.title {
					flex: 1;
					display: flex;
					flex-direction: column;
					margin-left: 32upx;

					.name {
						color: #222222;
						font-size: 40upx;
						font-family: PingFangSC-Semibold;
						font-weight: 600;
					}

					.idcard {
						width: 68upx;
						height: 32upx;
						line-height: 32upx;
						text-align: center;
						background: linear-gradient(270deg, rgba(250, 231, 87, 1) 0%, rgba(242, 203, 44, 1) 100%);
						;
						font-size: 18upx;
						color: #ff4b00;
						font-family: PingFangSC-Semibold;
						font-weight: 600;
						box-shadow: 0px 6px 20px 0px rgba(0, 0, 0, 0.03);
						border-radius: 16upx;
					}
				}

				.time {
					flex: 0 0 80upx;
					height: 80upx;
					display: flex;
					flex-direction: column;
					align-items: center;
					background: linear-gradient(180deg, rgba(250, 231, 87, 1) 0%, rgba(242, 203, 44, 1) 100%);
					border-radius: 8upx;

					.sendcard {
						color: #222222;
						font-size: 18upx;
						margin-top: 4upx;
					}

					.day {
						height: 42upx;
						width: 72upx;
						display: flex;
						margin-top: 4upx;
						justify-content: center;
						align-items: center;
						font-size: 24upx;
						background-color: #FFFFFF;
						border-radius: 2upx;
					}
				}
			}
		}

		.item-list {
			display: flex;
			justify-content: center;
			align-items: center;
			flex-direction: column;
			padding: 0 32upx;
			.item-list-content {
				display: flex;
				align-items: center;
				height: 104upx;
				width: 100%;
				background-color: #FFFFFF;
				border-radius:16upx;
				margin-bottom: 32upx;
				padding: 0 24upx;
				box-sizing: border-box;
				.item-img {
					flex: 0 0 44upx;
					height: 44upx;
				}

				.text {
					flex: 1;
					margin-left: 16upx;
					font-size: 28upx;
					font-family: PingFangSC-Regular;
					font-weight: 400;
					color: rgba(34, 34, 34, 1);
				}

				.arrow {
					flex: 0 0 24upx;
					height: 24upx;
				}

			}
		}

	}
</style>
