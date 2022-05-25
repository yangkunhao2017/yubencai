<template>
  <view>
	  <view class="bottom-box" :class="isUser?' bottom-box-user':'bottom-box-com'">
	  	<view class="uni-flex uni-row ">
	  		<view class="uni-seleton">
	  				<uni-icons  class="back-btn iconfont iconarrow_btn_left" type="arrowleft"   color="#fff" @click="navBack"/>
	  			</view>
	  		<view class="uni-flex title-text view-vertical-center" style="margin-bottom: 10px;margin-top: 10px;">
	  		<text v-if="isUser">修改登录密码</text>
	  		<text v-else="isUser">修改登录密码</text>
	  		</view>
	  	</view>
	  </view>
    <view className="uni-flex uni-column view-center" style="margin-top: 50px;">
      <view className="uni-flex uni-row input-box view-center">
        <uni-icons type="phone-filled"></uni-icons>
        <input className="input-input" placeholder="请输入手机号"/>
        <uni-icons type="closeempty"></uni-icons>
      </view>
      <view className="uni-flex uni-row input-box view-center">
        <uni-icons type="locked-filled"></uni-icons>
        <input className="input-input" password="true" placeholder="请输入密码"/>
        <uni-icons type="closeempty"></uni-icons>
      </view>
      <view className="uni-flex uni-row input-box view-center">
        <uni-icons type="locked-filled"></uni-icons>
        <input className="input-input" password="true" placeholder="请输入密码"/>
        <uni-icons type="closeempty"></uni-icons>
      </view>
      <view className="uni-flex uni-row input-box view-center">
        <uni-icons type="locked-filled"></uni-icons>
        <input className="input-input" placeholder="请输入验证码"/>
        <text>发送验证码</text>
      </view>
    </view>
    <view style="margin-top: 30px;">
      <button v-if="isUser" type="primary" className="submit-button">提交</button>
	   <button v-else="isUser" type="primary" className="submit-button-qi">提交</button>
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
.logo-img {
  width: 200px;
  height: 80px;
}

.input-box {
  /* #ifndef APP-NVUE */
  display: flex;
  /* #endif */
  padding: 10px 5px;
  flex-direction: row;
  flex-wrap: nowrap;
  background-color: #ffffff;
  margin-top: 30rpx;
  width: 80vw;
  border: 2px solid #efefef;
}

.input-input {
  height: 28px;
  line-height: 28px;
  font-size: 15px;
  padding: 0px;
  flex: 1;
  background-color: #ffffff;
}

.submit-button {
  width: 80vw;
  border-radius: 10rpx;
  background-image: linear-gradient(to right, #3B92FF, #3958E1);
}
.submit-button-qi {
  width: 80vw;
  border-radius: 10rpx;
  background-image: linear-gradient(to right, #fc4039, #fc4039);
}
</style>
