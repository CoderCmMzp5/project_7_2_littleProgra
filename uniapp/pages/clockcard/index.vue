<template>
	<view class="content">
		<Index/>
		<view class="model" v-if="isShowModel">
			<view class="model-wrapper">
				<view class="title">今天是</view>
				<view class="time">5月5日 星期日</view>
				<view class="model-send">
					<view class="same-icon" @click="_goToClockDetail">
						<image class="img-icon" src="../../static/images/card.png" mode=""></image>
						<text class="text">打卡</text>
					</view>
					<view class="same-icon">
						<image class="img-icon" src="../../static/images/share.png" mode=""></image>
						<text class="text">分享</text>
					</view>
					<view class="same-icon">
						<image class="img-icon" src="../../static/images/invite.png" mode=""></image>
						<text class="text">邀请</text>
					</view>
				</view>
				<view class="block"></view>
				<image class="close" src="../../static/images/close.png" mode="" @click="_closeModel"></image>
			</view>
		</view>
	</view>
</template>

<script>
	// import Index from "../../wxcomponents/index.vue";
	import Index from '../common/index'
	import { PAGE_CLOCK_DETAIL } from '../../static/page-path.js'
	export default {
		components:{
			'Index' : Index
		},
		data() {
			return {
				isShowModel: true
			}
		},
		created(){
		},
		onLoad() {
			this.backBottom()
		},
		onShow(){
			
		},
		methods: {
			backBottom: function(){
				wx.pageScrollTo({
					scrollTop: 300
				})
			},
			/*
			* 关闭弹框
			* */
			_closeModel(){
				this.$data.isShowModel = false
			},
			//去打卡详情页面
			_goToClockDetail(){
				uni.navigateTo({
					url:PAGE_CLOCK_DETAIL
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
	.content{
		padding-bottom: 64upx;
		.model{
			position: fixed;
			top: 0;
			left: 0;
			right: 0;
			bottom: 0;
			background-color: rgba(0,0,0,0.5);
			z-index: 10000;
			.model-wrapper{
				position: absolute;
				bottom: 30upx;
				left: 32upx;
				height: 330upx;
				width: 686upx;
				padding: 32upx 32upx 32upx 40upx;
				box-sizing: border-box;
				background-color: #FFFFFF;
				border-radius:8upx ;
				.title, .time{
					color: #222;
					font-size: 36upx;
					font-family: PingFangSC-Medium;
					font-weight: 500;
				}	
				.time{
					margin-top: 15upx;
				}			
				.model-send{
					margin-top: 40upx;
					padding:0 53upx;
					display: flex;
					justify-content: space-between;
					.same-icon{
						display: flex;
						flex-direction: column;
						justify-content: center;
						align-items: center;
						.img-icon{
							height: 64upx;
							width: 64upx;
						}
						.text{
							margin-top: 8upx;
							color: #999999;
							font-size: 24upx;
						}
					}
				}
				.block{
					height: 20upx;
					width: 20upx;
					position: absolute;
					bottom: 0;
					left: 50%;
					margin-left: -10upx;
					margin-bottom: -10upx;
					background-color: #FFFFFF;
					transform: rotate(45deg);
				}
				.close{
					position: absolute;
					top: 32upx;
					right: 32upx;
					height: 36upx;
					width: 36upx;
				}
			}
		}
		
	}
</style>
