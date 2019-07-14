<template>
	<div class='wrapper'>
		<view class="content">
			<image class="img-icon" src="../../static/images/author-icon.png" mode=""></image>
			<text class="name">萧梵俊</text>
			<text class="desc">于2019-08-27获得书虫称号</text>
			<image class="level" src="../../static/images/level1.png" mode=""></image>
		</view>
		<view class="share">
			<view class="common">
				<image src="../../static/images/wechart.png" mode=""></image>
				<text class="text">微信好友</text>
			</view>
			<view class="common">
				<image src="../../static/images/friend.png" mode=""></image>
				<text class="text">朋友圈</text>
			</view>
			<view class="common">
				<image src="../../static/images/saveimg.png" mode=""></image>
				<text class="text">保存图片</text>
			</view>
			<view class="common">
				<image src="../../static/images/copy.png" mode=""></image>
				<text class="text">复制链接</text>
			</view>
		</view>
	</div>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			
		}
	}
</script>

<style lang="scss" scoped>
	.wrapper{
		background-color: #f5f5f5;
		padding: 32upx;
		box-sizing: border-box;
		padding-bottom: 80upx;
		width: 100%;
		min-height: 100%;
		.content{
			background-color: #fff;
			border-radius: 15upx;
			padding: 64upx 0 96upx 0;
			box-sizing: border-box;
			display: flex;
			flex-direction: column;
			justify-content: center;
			width: 100%;
			align-items: center;
			box-sizing: border-box;
			.img-icon{
				height: 160upx;
				width: 160upx;
			}
			.name{
				margin-top: 32upx;
				color: #222;
				font-size: 42upx;
				font-weight: 600;
				
			}
			.desc{
				margin-top: 16upx;
				color: #B035E4;
				font-size: 30upx;
				font-weight: 400;
			}
			.level{
				height: 480upx;
				width: 480upx;
				margin-top: 68upx;
			}
		}
		.share{
			margin-top: 60upx;
			display: flex;
			justify-content: space-between;
			align-items: center;
			margin-left: 20upx;
			margin-right: 20upx;
			.common{
				display: flex;
				flex-direction: column;
				justify-content: center;
				align-items: center;
				image{
					height: 44upx;
					width: 44upx;
				}
				.text{
					margin-top: 16upx;
					font-size: 28upx;
					color: #222;
				}
			}
		}
	}
</style>
