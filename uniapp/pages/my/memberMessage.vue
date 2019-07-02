<template>
	<div class="wrapper">
		<view class="student-msg">
			<text class="title">学生信息</text>
			<view class="msg-detail">
				<view class="msg">
					<text class="right">头像</text>
					<view class="img">
						<image src="../../static/images/author-icon.png" mode=""></image>
					</view>
					<image  class="arrow" src="../../static/images/arrow_icon_1.png" mode=""></image>
				</view>
				
				<view class="msg">
					<text class="right">姓名</text>
					<input type="text" value="萧梵俊" disabled class="input"/>
					<image  class="arrow" src="../../static/images/arrow_icon_1.png" mode=""></image>
				</view>
				
				<view class="msg-1">
					<text class="right">出生日期</text>
					<input type="text" placeholder="2019-02-22"  disabled class="input"/>
				</view>
				
				<view class="msg">
					<text class="right">学校</text>
					<input type="text" value="上海交通大学附属小学" disabled class="input"/>
					<image  class="arrow" src="../../static/images/arrow_icon_1.png" mode=""></image>
				</view>
				
				<view class="msg">
					<text class="right">班级</text>
					<input type="text" value="一年级六班" disabled class="input"/>
					<image  class="arrow" src="../../static/images/arrow_icon_1.png" mode=""></image>
				</view>
				
			</view>
		</view>
		
		<view class="student-msg">
			<text class="title">监护人信息</text>
			<view class="msg-detail">
				<view class="msg">
					<text class="right">萧继凌  (父亲)</text>
					<input type="text" value="15325732408" disabled class="input"/>
					<image  class="arrow" src="../../static/images/arrow_icon_1.png" mode=""></image>
				</view>
			</view>
		</view>
	</div>
</template>

<script>
</script>

<style scoped lang="scss">
	.wrapper{
		height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		padding: 32upx;
		box-sizing: border-box;
		.student-msg{
			.title{
				margin-left: 32upx;
				font-size: 24upx;
				font-weight: 500;
				color: #666;
			}
			.msg-detail{
				background-color: #fff;
				border-radius: 16upx;
				padding: 0 32upx;
				margin-top: 16upx;
				.msg{
					display: flex;
					align-items: center;
					height: 144upx;
					border-bottom: 1upx solid #eee;
					.right{
						flex: 0 0 200upx;
						text-align: left;
						color: #222;
						font-size: 28upx;
						font-weight: 500;
					}
					.img{
						flex: 1;
						display: flex;
						justify-content: flex-end;
						image{
							height: 80upx;
							width: 80upx;
						}
					}
					.input{
						flex: 1;
						text-align: right;
						font-size: 28upx;
						color: #222;
					}
					.arrow{
						flex: 0 0 36upx;
						height: 36upx;
						margin-left: 16upx;
					}
				}
				.msg-1{
					display: flex;
					align-items: center;
					height: 144upx;
					border-bottom: 1upx solid #eee;
					.right{
						flex: 0 0 120upx;
						text-align: left;
						color: #222;
						font-size: 28upx;
						font-weight: 500;
					}
					.input{
						flex: 1;
						text-align: right;
					}
				}
				.msg:nth-last-child(1){
					border: none
				}
			}
		
		}
		.student-msg:nth-of-type(2){
			margin-top: 20upx;
		}
	}
</style>
