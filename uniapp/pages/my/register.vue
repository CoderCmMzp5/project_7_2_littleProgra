<template>
	<div class="wrapper">
		<view class="student-msg">
			<text class="title">学生信息</text>
			<view class="msg-detail">
				
				
				<view class="msg">
					<text class="right">姓名</text>
					<input type="text" value="" placeholder="请输入您的姓名"   class="input"/>
				</view>
				
				<view class="msg-1">
					<text class="right">性别</text>
					<view class="boy">
						<image class="icon" src="../../static/images/boy.png" mode=""></image>
						<text class="sex">男生</text>
						<image class="select" src="../../static/images/hasread.png" mode=""></image>
					</view>
					<view class="girl">
						<image class="icon" src="../../static/images/girl.png" mode=""></image>
						<text class="sex">女生</text>
					</view>
				</view>
				
				<view class="msg">
					<text class="right">出生日期</text>
					<input type="text" placeholder="请选择您的出生日期"   class="input"/>
					<image class="arrow" src="../../static/images/date.png" mode=""></image>
				</view>
				
				<view class="msg">
					<text class="right">您的学校</text>
					<input type="text" placeholder='填写学校' value=""  class="input"/>
				</view>
				
				<view class="msg">
					<text class="right">您的班级</text>
					<input type="text" placeholder="填写班级" value=""  class="input"/>
				</view>
				
			</view>
		</view>
		
		<view class="student-msg">
			<text class="title">监护人信息</text>
			<view class="msg-detail">
				<view class="msg-2">
					<view class="content">
						<text class="right">姓名</text>
						<input type="text" value="" placeholder="您的姓名" placeholder-style="color:#bbb;" class="input"/>
					</view>
					<view class="content">
						<text class="right">关系</text>
						<input type="text" value="" placeholder="您和孩子的关系" placeholder-style="color: #bbb;" class="input"/>
					</view>
				</view>
				<view class="msg">
					<text class="right right1">电话</text>
					<input type="text" value="" placeholder="请输入您的手机号码" placeholder-style="color:#bbb;"  class="input"/>
				</view>
				<view class="msg-3">
					<view class="content">
						<image class="icon" src="../../static/images/register_add.png" mode=""></image>
						<text class="text">添加监护人</text>
					</view>
				</view>
				<view class="block" style="height: 32upx;"></view>
			</view>
		</view>
		<button type="primary" class="btn" @click="_goToMemberPage">提交</button>
	</div>
</template>

<script>
	import { PAGE_MEMBER_MESSAGE } from '../../static/page-path.js'
	export default{
		data(){
			return{
				
			}
		},
		methods: {
			_goToMemberPage(){
				uni.navigateTo({
					url: PAGE_MEMBER_MESSAGE
				})
			}
		}
	}
</script>

<style scoped lang="scss">
	.wrapper{
		min-height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		padding: 32upx;
		padding-bottom: 107upx;
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
					.right1{
						flex: 0 0 80upx;
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
						text-align: left;
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
					.boy, .girl{
						height: 98upx;
						width: 231upx;
						border: 1upx solid #AF9F19;
						border-radius: 16upx;
						display: flex;
						align-items: center;
						padding: 0 24upx;
						box-sizing: border-box;
						position: relative;
						margin-left: 80upx;
						.icon{
							height: 64upx;
							width: 64upx;
						}
						.sex{
							font-size: 24upx;
							color: #222;
							margin-left: 24upx;
						}
						.select{
							position: absolute;
							bottom: 0;
							right: 0;
							height: 36upx;
							width: 48upx;
						}
					}
					.girl{
						border: none;
						margin-left: 0upx;
						padding-left: 40upx;
					}
				}
				.msg-2{
					display: flex;
					justify-content: space-between;
					height: 144upx;
					align-items: center;
					.content{
						display: flex;
						align-items: center;
						height: 100%;
						border-bottom: 1upx solid #eee;
						.right{
							flex: 0 0 60;
							color: #222;
							font-size: 28upx;
							font-weight: 500;
						}
						.input{
							margin-left: 30upx;
							flex: 1;
							font-size: 28upx;
							color: #666
						}
					}
					.content:nth-of-type(2){
						margin-left: 48upx;
					}
				}
				.msg-3{
					height: 80upx;
					width: 100%;
					border: 1upx dashed #ddd;
					display: flex;
					justify-content: center;
					align-items: center;
					border-radius: 16upx;
					margin-top: 32upx;
					.icon{
						height: 24upx;
						width: 24upx;
					}
					.text{
						color: #999;
						font-size: 28upx;
						margin-left: 8upx;
					}
				}
			}
		}
		.student-msg:nth-of-type(2){
			margin-top: 20upx;
		}
		.btn{
			height: 94upx;
			width: 100%;
			line-height: 94upx;
			background: linear-gradient(225deg,rgba(247,234,122,1) 0%,rgba(241,187,0,1) 100%);
			color: #222;
			font-size: 28upx;
			margin-top: 40upx;
			box-shadow:0px 6px 20px 0px rgba(0,0,0,0.03);
			border-radius: 16upx;
		}
		button:after{
			border: none;
		}
	}
</style>
