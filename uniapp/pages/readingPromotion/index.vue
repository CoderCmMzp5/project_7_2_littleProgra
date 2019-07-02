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
			<text class="text">风筝下的古树</text>
			<text class="name">古山哈哈哈哈哈哈</text>
			<image class="icon" src="../../static/images/noread.png" mode=""></image>
		</view>
		
		<view class="content">
			<image src="../../static/images/book-img.png" mode="" class="book-img"></image>
			<text class="text">风筝下的古树</text>
			<text class="name">古山哈哈哈哈哈哈很多很多和</text>
			<image class="icon" src="../../static/images/clock.png" mode=""></image>
		</view>
	</div>
</template>

<script>
	import { PAGE_PROMOTION_DETAIL, PAGE_NICE_PROMOTION} from '../../static/page-path.js'
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			_goToPromotionDetail(){
				uni.navigateTo({
					url:PAGE_PROMOTION_DETAIL
				})
			},
			_goToNicePromotion(){
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
				color: #999;
				font-size: 24upx;
				text-align: center;
				width: 100%;
				overflow: hidden;
				white-space: nowrap;
				text-overflow: ellipsis;;
				margin-top: 8upx;
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
