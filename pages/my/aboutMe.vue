<template>
	<div class='wrapper'>
		<div class='content'>
			<image src="https://r.ffimg.cn/hlswx/2019-07-04/5d1df931acdf1231028041.png" mode="" class="img-iocn"></image>
			<image src="../../static/images/my-icon.png" mode="" class="company-icon"></image>
			<view class="text">
				<view class="text-1">企业简介是指通过文字和图片资料向社会公众介绍企业基本情况和经营战略的文案。主要介绍企业名称、企业的法律性质、开办地址、设立时间、所属行业、注册资金、建筑面积、技术装备条件；生产经营范围、主要产品结构；企业发展战略、经营理念等情况。</view>
				<view class="text-2">企业简介是指通过文字和图片资料向社会公众介绍企业基本情况和经营战略的文案。</view>
				<view class="text-1">主要介绍企业名称、企业的法律性质、开办地址、设立时间、所属行业、注册资金、建筑面积、技术装备条件；生产经营范围、主要产品结构；企业发展战略、经营理念等情况。</view>
			</view>
		</div>
	</div>
</template>

<script>
</script>

<style lang="scss" scoped>
	.wrapper {
		min-height: 100%;
		width: 100%;
		padding: 32upx;
		background-color: #f5f5f5;
		box-sizing: border-box;
		.content{
			height: 1080upx;
			width: 100%;
			position: relative;
			.img-iocn {
				position: absolute;
				height: 100%;
				width: 100%;
				z-index: 1;
			}
			.company-icon{
				position: relative;
				top: 64upx;
				left: 283upx;
				z-index: 100;
				height: 160upx;
				width: 120upx;
			}
			.text{
				position: relative;
				margin-top: 120upx;
				z-index: 100;
				color: #333;
				font-size: 24upx;
				padding: 0 32upx;
				box-sizing: border-box;
				line-height: 48upx;
				.text-2{
					margin: 32upx 0;
				}
			}
			
		}
	}
</style>
