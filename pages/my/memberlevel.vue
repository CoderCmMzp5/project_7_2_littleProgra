<template>
	<div class='wrapper'>
		<view class="content" @click="_GoToLevelDetail">
			<image src="../../static/images/level1.png" mode="" class="book-img"></image>
			<text class="text">书虫</text>
			<text class="desc active">于2019-08-27获得</text>
		</view>
		
		<view class="content">
			<image src="../../static/images/level2.png" mode="" class="book-img"></image>
			<text class="text">书虫</text>
			<text class="desc">尚未获得</text>
		</view>
		
		<view class="content">
			<image src="../../static/images/level3.png" mode="" class="book-img"></image>
			<text class="text">书虫</text>
			<text class="desc">尚未获得</text>
		</view>
		
		<view class="content">
			<image src="../../static/images/level4.png" mode="" class="book-img"></image>
			<text class="text">书虫</text>
			<text class="desc">尚未获得</text>
		</view>
		
		<view class="content">
			<image src="../../static/images/level5.png" mode="" class="book-img"></image>
			<text class="text">书虫</text>
			<text class="desc">尚未获得</text>
		</view>
		
		
	</div>
</template>

<script>
	import { PAGE_LEVEL_DETAIL } from '../../static/page-path.js'
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			//去等级详情
			_GoToLevelDetail(){
				uni.navigateTo({
					url:PAGE_LEVEL_DETAIL
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
		padding: 32upx;
		box-sizing: border-box;
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		align-content: flex-start;
		.content{
			height: 428upx;
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
				height: 240upx;
				width: 240upx;
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
			.desc{
				font-size: 24upx;
				color: #999;
				font-weight: 400;
				margin-top: 3upx;
			}
			.active{
				color: #B035E4
			}
		} ;
		
	}
</style>
