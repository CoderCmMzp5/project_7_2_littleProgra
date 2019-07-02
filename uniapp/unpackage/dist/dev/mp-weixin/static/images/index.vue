<template>
	<div class='wrapper'>
		<view class="content" @click="_goToPromotionDetail">
			<image src="../../static/images/book-img.png" mode="" class="book-img"></image>
			<text class="text">风筝下的古树</text>
			<text class="name">古三</text>
			<image class="icon" src="../../static/images/hasread.png" mode=""></image>
		</view>
		
		<view class="content" @click="_goToNicePromotion">
			<image src="../../static/images/book-img.png" mode="" class="book-img"></image>
			<text class="text">风筝下的古树哈哈哈哈哈哈</text>
			<text class="name">古三</text>
			<image class="icon" src="../../static/images/noread.png" mode=""></image>
		</view>
		
		<view class="content">
			<image src="../../static/images/book-img.png" mode="" class="book-img"></image>
			<text class="text">风筝下的古树</text>
			<text class="name">古三</text>
			<image class="icon" src="../../static/images/clock.png" mode=""></image>
		</view>
	</div>
</template>

<script>
	import {PAGE_PROMOTION_DETAIL, PAGE_NICE_PROMOTION} from '../../static/page-path.js'
	export default{
		data() {
			return {
		
			}
		},
		onLoad() {
		
		},
		methods: {
			_goToPromotionDetail(){
				console.log(PAGE_PROMOTION_DETAIL)
				uni.navigateTo({
					url:PAGE_PROMOTION_DETAIL
				})
			},
			//好书推荐
			_goToNicePromotion(){
				console.log(PAGE_NICE_PROMOTION)
				uni.navigateTo({
					url:PAGE_NICE_PROMOTION
				})
			}
		}
	}
	
</script>

<style lang="scss" scoped>
	.wrapper{
		height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		padding: 32upx;
		box-sizing: border-box;
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		align-content: flex-start;
		.content{
			height: 444upx;
			width: 327upx;
			background-color: #FFFFFF;
			margin-bottom: 32upx;
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			border-radius:16upx;
			position: relative;
			padding: 0 24upx;
			box-sizing: border-box;
			.book-img{
				height: 260upx;
				width: 200upx;
			}
			.text{
				color: #222222;
				font-size: 28upx;
				font-family: PingFangSC-Medium;
				font-weight: 500;
				margin-top: 32upx;
				width: 100%;
				text-align: center;
				overflow: hidden;
				white-space: nowrap;
				text-overflow: ellipsis;
			}
			.name{
				font-size: 24upx;
				color: #999999;
				font-family: PingFangSC-Regular;
				margin-top: 16upx;
			}
			.icon{
				height: 36upx;
				width: 48upx;
				position: absolute;
				bottom: 0;
				right: 0;
			}
		} ;
		
	}
</style>
