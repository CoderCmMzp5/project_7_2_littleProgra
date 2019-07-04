<template>
	<view class="wrapper">
		<view class="header">
			<image class="bg" src="../../static/images/home_bg.png" mode=""></image>
			<view class="content">
				<image class="headimg" src="../../static/images/author-icon.png" mode=""></image>
				<view class="title">
					<text class="name">清明雨上</text>
					<text class="idcard">书仙</text>
				</view>
				<view class="time">
					<text class="sendcard">打卡</text>
					<text class="day">36天</text>
				</view>
			</view>
		</view>
		<view class="item-list">
			<view class="item-list-content" @click="_goToMemberMessage">
				<image class="item-img" src="../../static/images/my-icon-1.png" mode=""></image>
				<text class="text">会员信息</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goToMemberCard">
				<image class="item-img" src="../../static/images/my-icon-2.png" mode=""></image>
				<text class="text">会员海报</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goToBookself">
				<image class="item-img" src="../../static/images/my-icon-3.png" mode=""></image>
				<text class="text">打卡书单</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goTomemberLevel" >
				<image class="item-img" src="../../static/images/my-icon-4.png" mode=""></image>
				<text class="text">晋级奖励</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goToConfirm">
				<image class="item-img" src="../../static/images/my-icon-5.png" mode=""></image>
				<text class="text">月阅计划</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>

			<view class="item-list-content" @click="_goToAboutMe">
				<image class="item-img" src="../../static/images/my-icon-6.png" mode=""></image>
				<text class="text">关于我们</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>
			<view class="item-list-content" @click="togglePopup('bottom-share')" data-position="bottom">
				<image class="item-img" src="../../static/images/my-icon-5.png" mode=""></image>
				<text class="text">分享</text>
				<image class="arrow" src="../../static/images/arrow-icon.png" mode=""></image>
			</view>
		</view>
	
		<view class="example">
			<uni-popup :show="type === 'middle-img'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img2')">
					<image class="image" src="https://r.ffimg.cn/hlswx/2019-07-04/5d1dfbe1c2a3c139804699.png" />
					<view class="centerBox">
						<view>恭喜过关</view>
						<view>加油你是最棒的</view>
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img2'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img3')">
					<view class="centerBox centerBoxInner">
						<view>恭喜获得书虫称号</view>
						<view>你已成功打卡36天</view>
						<image class="image innerImgs" src="../../static/images/pop_2.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img3'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img4')">
					<view class="centerBox centerBoxInner">
						<view>恭喜获得书迷称号</view>
						<view>你已成功打卡36天</view>
						<image class="image innerImgs" src="../../static/images/pop_3.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img4'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img5')">
					<view class="centerBox centerBoxInner">
						<view>恭喜获得书霸称号</view>
						<view>你已成功打卡36天</view>
						<image class="image innerImgs" src="../../static/images/pop_4.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img5'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img6')">
					<view class="centerBox centerBoxInner">
						<view>恭喜获得书王称号</view>
						<view>你已成功打卡36天</view>
						<image class="image innerImgs" src="../../static/images/pop_5.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img6'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img7')">
					<view class="centerBox centerBoxInner">
						<view>恭喜获得书仙称号</view>
						<view>你已成功打卡36天</view>
						<image class="image innerImgs" src="../../static/images/pop_6.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img7'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img8')">
					<view class="centerBox centerBoxInner">
						<view>打卡</view>
						<view>你已经36天没有打卡了</view>
						<image class="image innerImgs" src="../../static/images/pop_7.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img8'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img9')">
					<view class="centerBox centerBoxInner">
						<view>恭喜获得补签卡</view>
						<view>恭喜您获得一张补签卡</view>
						<image class="image innerImgs" src="../../static/images/pop_8.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img9'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img10')">
					<view class="centerBox centerBoxInner">
						<view>打卡成功</view>
						<view>你已经成功打卡36天</view>
						<image class="image innerImgs" src="../../static/images/pop_9.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img10'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img11')">
					<view class="centerBox centerBoxInner">
						<view>推荐成功</view>
						<view>你已经成功推荐XXX</view>
						<image class="image innerImgs" src="../../static/images/pop_10.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			<uni-popup :show="type === 'middle-img11'" position="middle" mode="insert" >
				<view class="uni-center center-box"  @click="togglePopup('middle-img12')">
					<view class="centerBox centerBoxInner">
						<view>推荐失败</view>
						<view style="color: #cccccc;">你推荐XXX失败</view>
						<image class="image innerImgs" src="../../static/images/pop_11.png" />
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			
			<uni-popup :show="type === 'middle-img12'" position="middle" mode="insert" >
				<view class="uni-center center-box">
					<image class="image innerImgs fullBg" style="margin-top: 0;" src="https://r.ffimg.cn/hlswx/2019-07-04/5d1dfa11b87fb059237444.png"/>
					<view class="centerBox centerBoxInner" style="top:20upx;">
						<view class="fullBg_title">
							<image class="image innerImgs" src="../../static/images/bg_y.png" />
							<view>解锁书籍</view>
						</view>
						 <image src="https://r.ffimg.cn/hlswx/2019-07-04/5d1e00aac0888283293860.png" class="fullBg_bImg_1"></image>
						<view class="fullBg_bTitle_1">闲适的时光</view>
						<view class="fullBg_bTitle_2">人民出版社</view>
					</view>
				</view>
				<view class="close-box"  @click="hidePopup('')">
					<image src="../../static/images/close.png"></image>
				</view>
			</uni-popup>
			
			
			<uni-popup :show="type === 'bottom-share'" position="bottom" @hidePopup="togglePopup('')">
				<view class="bottom-title">分享到</view>
				<view class="bottom-content">
					<view class="bottom-content-box" v-for="(item, index) in bottomData" :key="index">
						<view class="bottom-content-image" :class="item.name">
							<image :src="getImgUrl(item.icon)" class="fxImg"></image>
						</view>
						<view class="bottom-content-text">{{ item.text }}</view>
					</view>
				</view>
				<view class="bottom-btn" @click="hidePopup('')">取消分享</view>
			</uni-popup>
		</view>
	</view>


</template>

<script>
	import uniPopup from '@/pages/my/uni-popup.vue'
	import { PAGE_MEMBER_MESSAGE, PAGE_MEMBER_CARD ,PAGE_BOOKSELF, PAGE_MEMBER_LEVEL, PAGE_ABOUT_ME, PAGE_REGIESTER} from '../../static/page-path.js'
	export default {
		components: {
			uniPopup
		},
		data() {
			return {
				tkType:0,
				type: '',
				list: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10'],
				bottomData: [{
						text: '朋友圈',
						icon: 'logo_1',
						name: 'wx'
					},
					{
						text: '微信',
						icon: 'logo_2',
						name: 'wx'
					},
					{
						text: '新浪微博',
						icon: 'logo_3',
						name: 'qq'
					},
					{
						text: 'QQ好友',
						icon: 'logo_4',
						name: 'sina'
					},
					{
						text: 'QQ空间',
						icon: 'logo_5',
						name: 'copy'
					},
					{
						text: '复制链接',
						icon: 'logo_6',
						name: 'more'
					},
					{
						text: '浏览器打开',
						icon: 'logo_7',
						name: 'more'
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
			//去会员信息
			_goToMemberMessage(){
				uni.navigateTo({
					url: PAGE_REGIESTER
				})
			},
			//去会员海报页面
			_goToMemberCard(){
				uni.navigateTo({
					url:PAGE_MEMBER_CARD
				})
			},
			//去打卡书单页面
			_goToBookself(){
				uni.navigateTo({
					url:PAGE_BOOKSELF
				})
			},
			//去会员等级页面
			_goTomemberLevel(){
				uni.navigateTo({
					url: PAGE_MEMBER_LEVEL
				});
			},
			//去关于我们
			_goToAboutMe(){
				uni.navigateTo({
					url:PAGE_ABOUT_ME
				})
			},
			//所有弹框
			_goToConfirm(){
				var that=this;
				uni.showModal({
					content: "您有新的奖励",
					confirmText: "查看",
					cancelText: "取消",
					cancelColor:'#adadad',
					confirmColor:'#F3D03F',
					success:function(){
						that.togglePopup('middle-img')
					}
				})
			},
			togglePopup(type) {
				uni.hideTabBar()  
				this.type = type;
			},
			hidePopup(type){
				this.type = type;
				uni.showTabBar()
			},
			getImgUrl(icon){
			  return require("../../static/images/"+icon+".png");
			}
		}
	}
</script>

<style lang="scss" scoped>
	.example {
		padding: 0 30upx 30upx
	}
	.centerBox{
		position: absolute;
		top:90upx;
		text-align: center;
		width: 100%;
	}
	.centerBox view:nth-of-type(1){
		color: #383838;
		font-weight: bold;
		padding-top:10upx;
		font-size: 65upx;
	}
	.centerBox view:nth-of-type(2){
		font-size: 35upx;
		color: #d9c51a;
		padding-bottom:10upx;
	}
	.centerBoxInner view:nth-of-type(2){
		padding-top:24upx;
	}
	.innerImgs{
		width: 450upx!important;
		height: 450upx!important;
		margin:0 auto;
		margin-top: 24upx;
	}
	.fullBg{
		width:100%!important;
		height:100%!important;
		position:absolute!important;
		top:0!important;
		left:0!important;
	}
	.fullBg_title{
		width:400upx!important;
		height:100upx!important;
		position:absolute!important;
		left:50%!important;
		top:20upx!important;
		margin-left:-200upx!important;
		font-size:30upx!important;
		color:#726816!important;
	}
	.fullBg_title image{
		width: 100%!important;
		height:100upx!important;
	}
	.fullBg_title view{
		position: absolute;
		width: 200upx;
		text-align: center;
		left:50%;
		margin-left:-100upx; 
		top:45upx;
		font-size: 35upx!important;
	}
	.fullBg_bImg_1{
		width:270upx;
		height: 370upx;
		margin:0 auto;
		
		margin-top:180upx;
		
	}
	.fullBg_bTitle_1{
		color:#373736!important;
		font-size:50upx!important;
		margin:0 auto;
		margin-bottom: 10upx;
		font-weight: bold
	}
	.fullBg_bTitle_2{
		color:#70706f!important;
		font-size:18upx;
		margin:0 auto;
	}
	.close-box{
		position: absolute;
		top:850upx;
		width: 100upx;
		height:100upx;
		margin:0 auto;
		background: #818181;
		border-radius: 50%;
		display: flex;
		align-items: center;
		justify-content: center
	}
	.close-box image{
		width:50upx;
		height: 50upx;
		
	}
	.fxImg{
		width: 100%!important;
		height:100%!important;
	}
	.example-title {
		font-size: 32upx;
		line-height: 32upx;
		color: #777;
		margin: 40upx 25upx;
		position: relative
	}
	
	.example .example-title {
		margin: 40upx 0
	}
	
	.example-body {
		padding: 0 40upx
	}
	
	.uni-padding-wrap {
		padding: 0 30upx;
	}
	
	button {
		margin: 20upx 0;
	}
	
	.uni-helllo-text {
		height: 100upx;
		line-height: 100upx;
		text-align: center;
	}
	
	.center-box {
		width: 600upx;
		height: 800upx;
		background: #fff;
		border-radius: 20upx;
	}
	.uni-list-item {
		text-align: left;
		line-height: 80upx;
		border-bottom: 1px #f5f5f5 solid;
	}
	
	.uni-list-item:last-child {
		border: none;
	}
	
	.center-box .image {
		width: 100%;
		height: 100%;
	}
	
	.bottom-title {
		line-height: 60upx;
		font-size: 24upx;
		padding: 30upx 0;
	}
	
	.bottom-content {
		display: flex;
		flex-wrap: wrap;
		padding: 0 30upx;
	}
	
	.bottom-content-box {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-bottom: 15upx;
		width: 25%;
		box-sizing: border-box;
	}
	
	.bottom-content-image {
		display: flex;
		justify-content: center;
		align-items: center;
		width:70upx;
		height:70upx;
		overflow: hidden;
		border-radius: 10upx;
	}
	
	.bottom-content-text {
		font-size: 26upx;
		color: #4c4c4c;
		line-height: 60upx;
		height: 60upx;
	}
	
	.bottom-btn {
		height: 90upx;
		line-height: 90upx;
		border-top: 1px #f5f5f5 solid;
		font-size: 30upx;
	}
	
	
	
	@font-face {
		font-family: 'iconfont';
		/* project id 1028200 */
		src: url('https://at.alicdn.com/t/font_1028200_47ewtwy4t04.ttf') format('truetype');
	}
	
	.icon {
		font-family: 'iconfont';
		font-size: 40upx;
		color: #fff;
	}
	.wrapper {
		min-height: 100%;
		width: 100%;
		background-color: #f5f5f5;
		.header {
			position: relative;
			padding: 14upx 32upx 18upx 32upx;
			margin-bottom: 32upx;
			.bg {
				position: absolute;
				top: 0;
				left: 0;
				width: 100%;
				height: 224upx;
				z-index: 10;
			}

			.content {
				height: 192upx;
				width: 100%;
				display: flex;
				align-items: center;
				padding: 32upx;
				background-color: #FFFFFF;
				border-radius: 16upx;
				box-sizing: border-box;
				position: relative;
				z-index: 100;
				.headimg {
					flex: 0 0 128upx;
					height: 128upx;

				}

				.title {
					flex: 1;
					display: flex;
					flex-direction: column;
					margin-left: 32upx;

					.name {
						color: #222222;
						font-size: 40upx;
						font-family: PingFangSC-Semibold;
						font-weight: 600;
					}

					.idcard {
						width: 68upx;
						height: 32upx;
						line-height: 32upx;
						text-align: center;
						background: linear-gradient(270deg, rgba(250, 231, 87, 1) 0%, rgba(242, 203, 44, 1) 100%);
						;
						font-size: 18upx;
						color: #ff4b00;
						font-family: PingFangSC-Semibold;
						font-weight: 600;
						box-shadow: 0px 6px 20px 0px rgba(0, 0, 0, 0.03);
						border-radius: 16upx;
					}
				}

				.time {
					flex: 0 0 80upx;
					height: 80upx;
					display: flex;
					flex-direction: column;
					align-items: center;
					background: linear-gradient(180deg, rgba(250, 231, 87, 1) 0%, rgba(242, 203, 44, 1) 100%);
					border-radius: 8upx;

					.sendcard {
						color: #222222;
						font-size: 18upx;
						margin-top: 4upx;
					}

					.day {
						height: 42upx;
						width: 72upx;
						display: flex;
						margin-top: 4upx;
						justify-content: center;
						align-items: center;
						font-size: 24upx;
						background-color: #FFFFFF;
						border-radius: 2upx;
					}
				}
			}
		}

		.item-list {
			display: flex;
			justify-content: center;
			align-items: center;
			flex-direction: column;
			padding: 0 32upx;
			.item-list-content {
				display: flex;
				align-items: center;
				height: 104upx;
				width: 100%;
				background-color: #FFFFFF;
				border-radius:16upx;
				margin-bottom: 32upx;
				padding: 0 24upx;
				box-sizing: border-box;
				.item-img {
					flex: 0 0 44upx;
					height: 44upx;
				}

				.text {
					flex: 1;
					margin-left: 16upx;
					font-size: 28upx;
					font-family: PingFangSC-Regular;
					font-weight: 400;
					color: rgba(34, 34, 34, 1);
				}

				.arrow {
					flex: 0 0 24upx;
					height: 24upx;
				}

			}
		}

	}
</style>
