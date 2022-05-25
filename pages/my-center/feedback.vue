<template>
	<view>
		<view class="bottom-box" :class="isUser?' bottom-box-user':'bottom-box-com'">
			<view class="uni-flex uni-row ">
				<view class="uni-seleton">
						<uni-icons  class="back-btn iconfont iconarrow_btn_left" type="arrowleft"   color="#fff" @click="navBack"/>
					</view>
				<view class="uni-flex title-text view-vertical-center" style="margin-bottom: 10px;margin-top: 10px;">
				<text v-if="isUser">意见反馈</text>
				<text v-else="isUser">意见反馈</text>
				</view>
			</view>
		</view>
    <view style="border-bottom: 12px solid #dedddd;"></view>
		<view style="background-color: #FFFFFF">
		  <view class="uni-flex  uni-column   list-item">
		    <text style="font-size: 18px;margin-top: 10px;margin-left: 10px;">标题:</text>
			<view class="bottom-title uni-flex " >
			  <text class="tian-text" style="margin-top: 10px;margin-left: 20px;">请输入您的意见标题(20字以内)</text>
			</view> 
			</view>
		</view>
		<view class="uni-flex  uni-column   list-item">
		  <text style="font-size: 18px;margin-top: 10px;margin-left: 10px;">内容:</text>
			<view class="bottom-box uni-flex " >
			  <text class="tian-text" style="margin-top: 10px;margin-left: 20px;">请输入您的意见或建议(500字以内)</text>
			</view>
		</view>
		<view class="uni-flex  uni-column   list-item">
		  <text style="font-size: 18px;margin-top: 10px;margin-left: 10px;">上传截图:</text>
		<view class="bottom-jie uni-flex view-center " >
			<view class="example-body" >
				<uni-file-picker  limit="9" ></uni-file-picker>
			</view>
		</view>
		</view>
			<view class=" uni-flex view-vertical-center" >
			  <button v-if="isUser" class="button-info" style="margin-top: 80px;margin-bottom: 10px;">提交</button>
			  <button v-else="isUser" class="button-info-qi" style="margin-top: 80px;margin-bottom: 10px;">提交</button>
			</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isUser:false,
			}
		},
		methods: {
			// 返回上一页
				navBack() {
					uni.navigateBack();
				}
		}
	}
</script>

<style>
.bottom-box {
		width: 100%;
	  /* height: 80px; */
	  
	}
	.bottom-box-com {
		background: #fc4039;
	}
	.bottom-box-user {
		background-color: #0c7cf9;
	}
.bottom-title {
	width: 95%;
	height: 50px;
	background-color: #ececec;
	margin: auto;
	margin-top: 10px;
}
.bottom-jie {
	width: 95%;
	height: 250px;
	background-color: #dedede;
	margin: auto;
	margin-top: 10px;
}
.tian-text {
  color: #b4b6b6;
  font-size: 18px;
}
.button-info{
  background-color: #0c7cf9;
  color: white;
  width:95%;
}
.button-info-qi{
  background-color: #fc4039;
  color: white;
  width:95%;
}
.example-body {
		/* padding: 10px; */
		/* padding-top: 0; */
		line-height:100px;
		width: 200px;
		/* margin-bottom: 20px; */
		margin-right: -20vh; 
		
	}
	.back-btn {
			width: 100%;
			position: absolute;
			z-index: 999;
			padding-top: var(--status-bar-height);
			padding-left: 20upx;
			padding-right: 20upx;
			top: 30upx;
			font-size: 40upx;
			color: #fff;
			display: flex;
			align-items: center;
			.nav-title {
				width: 590upx;
				text-align: center;
			}
		}
		.title-text {
			color: #FFFFFF;
			font-size: 18px;
			font-family: sans-serif;
			/* margin-top: 20px; */
		}
</style>
