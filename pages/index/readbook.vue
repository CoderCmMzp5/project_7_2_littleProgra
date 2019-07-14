<template>
	<view class="wrapper">
		<image src="https://r.ffimg.cn/hlswx/2019-07-04/5d1df8a2dbcd7849782267.png" mode="" class="img-icon"></image>
		<view class="desc">
			<view class="common">
				<image src="../../static/images/left.png" mode=""></image>
				<text class="text">上一页</text>
			</view>
			<view class="common">
				<text class="text">第一章-1/6</text>
			</view>
			<view class="common">
				<text class="text">下一页</text>
				<image src="../../static/images/left.png" mode=""></image>
			</view>
		</view>
		
		<view class="listen" @click="goToListenBook">
			<image src="../../static/images/listen.png" mode=""></image>
		</view>
		
	</view>
</template>

<script>
	import { PAGE_LISTEN_BOOK } from '../../static/page-path.js'
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			goToListenBook(){
				uni.navigateTo({
					url:PAGE_LISTEN_BOOK
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
		position: relative;
		.img-icon{
			height: 1304upx;
			width: 100%;
		}
		.desc{
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 32upx;
			.common{
				display: flex;
				align-items: center;
				image{
					height: 36upx;
					width: 36upx;
				}
				.text{
					color: #222;
					font-size: 24upx;
					font-family:PingFangSC-Regular;
					font-weight:400;
				}
			}
			.common:nth-of-type(1){
				image{
					transform: rotate(-180deg)
				}
			}
		}
		.listen{
			height: 98upx;
			width: 98upx;
			display: flex;
			justify-content: center;
			align-items: center;
			position: absolute;
			background-color: #fff;
			right: 32upx;
			bottom: 140upx;
			border-radius: 50%;
			image{
				width: 41upx;
				height: 48upx;
			}
		}
	}
</style>
