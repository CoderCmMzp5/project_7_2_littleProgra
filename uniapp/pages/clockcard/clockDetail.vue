<template>
	<view class="wrapper">
		<view class="date">
			<calendar :date="date" :selected="selected" :disable-before="true" :start-date="'2019-7-1'" :end-date="'2019-12-31'" @change="change"
			 @to-click="toClick">
			</calendar>
			<button type="primary" class="btn">立即打卡</button>
			<view class="block" style="height: 64upx;"></view>
		</view>
		<view class="buchong">
			<view class="left">
				<image src="../../static/images/buqian_icon.png" mode=""></image>
				<text class="type">补签卡</text>
				<text class="count">剩余3张</text>
			</view>
			<view class="">
				<button type="primary" class="btn">立即使用</button>
			</view>
		</view>
		<view class="desc">
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
    				date: '2019-7-5'
				}, {
					date: '2019-7-2'
				}, {
					date: '2019-7-3'
				}, {
					date: '2019-7-4'
					}]
				
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
	.wrapper{
		min-height: 100%;
		width: 100%;
		padding: 32upx;
		box-sizing: border-box;
		background-color: #f5f5f5;
		padding-bottom: 30upx;
		.date{
			border-radius: 16upx;
			background-color: #fff;
			.btn{
				height: 94upx;
				width: 622upx;
				border-radius: 16upx;
				background: linear-gradient(225deg,rgba(247,234,122,1) 0%,rgba(241,187,0,1) 100%);
				box-shadow:0px 10px 30px 0px rgba(247,231,115,0.5);
				margin-top: 49upx;
				color: #222;
				font-size: 28upx;
				font-weight: 500;
				line-height: 94upx;
			}
			button::after{
				border: none;
			}
		}
		.buchong{
			display: flex;
			justify-content: space-between;
			align-items: center;
			border-radius: 16upx;
			height: 104upx;
			width: 100%;
			margin-top: 32upx;
			padding: 0 32upx;
			box-sizing: border-box;
			background-color: #fff;
			.left{
				display: flex;
				align-items: center;
				image{
					height: 43upx;
					width: 64upx;
				}
				.type{
					color: #222;
					font-size: 28upx;
					font-weight: 500;
					margin-left: 16upx;
				}
				.count{
					color: #222;
					font-size: 28upx;
					font-weight: 400;
					margin-left: 16upx;
				}
				
			}
			.btn{
				height: 64upx;
				width: 175upx;
				line-height: 64upx;
				color: #222;
				font-size: 24upx;
				font-weight: 400;
				background:linear-gradient(225deg,rgba(247,234,122,1) 0%,rgba(241,187,0,1) 100%);
				box-shadow:0px 10px 30px 0px rgba(247,231,115,0.5);
				border-radius: 38upx;
				
			}
			button::after{
				border: none;
			}
			
		}
		.desc{
			padding: 32upx;
			box-sizing: border-box;
			display: flex;
			flex-direction: column;
			.title{
				color: #666;
				font-weight: 500;
				font-family:PingFangSC-Medium;
				font-size: 24upx;
			}
			.common{
				color: #999;
				font-size: 24upx;
				font-weight: 400;
				font-family:PingFangSC-Regular;
				margin-top: 16upx;
			}
		}
	}
</style>
