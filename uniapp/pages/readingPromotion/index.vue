<template>
	<div class='wrapper'>
		<view class="book-wrapper" @click="_goToPromotionDetail">
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
		<view class="book-wrapper" @click="_goToNicePromotion">
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
		min-height: 100%;
		width: 100%;
		background-color: #fff;
		padding: 32upx;
		box-sizing: border-box;
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
</style>
