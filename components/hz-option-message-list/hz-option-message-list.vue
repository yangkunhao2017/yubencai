<template>
	<view style="background-color: #f6f6f6;">
		<view class="uni-flex uni-row item-box" v-for="i in 5">
      <view class="logo-box">
        <image src="../../../static/logo.png" ></image>
      </view>
      <view class="index-box uni-flex uni-column">
        <view>
          <text class="message-title">重庆梦比优斯网络科技有限公司</text>
        </view>
        <view class="uni-flex uni-column message-box">
          <view class="uni-flex uni-row view-between">
            <view class="uni-flex uni-column" style="color: #b8b8b8;font-size: 15px;width: 90%">
              <text>邀请您加入市场部</text>
              <text class="uni-ellipsis">时间：2022-05-15 23:59:59</text>
            </view>
            <view v-if="type==1">
              <image src="../../../static/logo.png" ></image>
            </view>
          </view>
          <view v-if="type==0" class="uni-flex uni-row">
            <button style="border: 1px solid #F0F0F0">拒绝</button>
            <button style="background-color: #0c7cf9;color: #FFFFFF">同意</button>
          </view>
        </view>
      </view>
    </view>
	</view>
</template>

<script>
	export default {
		name:"hz-option-message-list",
		data() {
			return {
				type:0,
			};
		}
	}
</script>

<style>

/*去掉按钮边框*/
button:after{
  border: none;
}

.item-box{
  margin-top: 0px;
  margin-bottom: 20px;
}
.logo-box{
  margin-top: 10px;
  margin-left: 5px;
}

.logo-box image{
  width: 50px;
  height: 50px;
}

.index-box {
  margin-left: 10px;
  width: 70vw;
}

.message-box {
  background-color: #FFFFFF;
  border-radius: 15px;
  padding: 10px;
}

.message-box image{
  width: 50px;
  height: 50px;
}

.message-box button{
  width: 100px;
  background-color: #FFFFFF;
  height: 40px;
  font-size: 18px;
  margin-left: 10px;
}

</style>