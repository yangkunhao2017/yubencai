<template>
	<view style="background-color: #f6f6f6">
		<view class="uni-flex uni-row item-box">
      <button class="item-box-active">待查看</button>
      <button>已查看</button>
      <button>约面试</button>
      <button>不合适</button>
    </view>
    <view class="uni-flex uni-column">
      <view class="uni-flex uni-column item-item" v-for="i in 10">
        <view class="uni-flex uni-row view-between">
          <view class="uni-flex uni-column">
            <text style="font-size: 20px">java中级开发工程师</text>
            <text style="font-size: 15px">重庆梦比优斯网络科技有限公司</text>
          </view>
          <view style="margin: 10px;color: #ed8035">
            9K~15K
          </view>
        </view>
        <view class="uni-flex uni-row view-between">
          <view>
            <text style="font-size: 12px;color: #929292">2022-05-15 23:59:59 投递简历</text>
          </view>
          <view class="uni-flex" style="border: 1px solid #4c8ce7;width: 80px;height: 25px;color: #4c8ce7;">
            <view class="uni-flex view-vertical-center">
              <text v-if="status==0">未查看</text>
              <text v-if="status==1">已查看</text>
              <text v-if="status==2">待确认</text>
              <text v-if="status==3">已接受</text>
              <text v-if="status==4">已拒绝</text>
            </view>
          </view>
        </view>
        <view class="uni-flex uni-row item-option-box">
          <button><uni-icons type="contact" size="20"></uni-icons>联系HR</button>
          <button v-if="type==0"><uni-icons type="clear" size="20"></uni-icons>撤销投递</button>
          <button v-if="type==1" style="color: #4cd964"><uni-icons type="checkmarkempty" size="20"></uni-icons>接受邀约</button>
          <button v-if="type==1" style="color: #ff0000"><uni-icons type="closeempty" size="20"></uni-icons>拒绝邀约</button>
          <button v-if="type==2" ><uni-icons type="mail-open-filled" size="20"></uni-icons>查看面试信息</button>
        </view>
      </view>
    </view>
	</view>
</template>

<script>
	export default {
		name:"hz-message-send-list",
		data() {
			return {
        status:0,
				type: 3,
			};
		}
	}
</script>

<style>
/*去掉按钮边框*/
button:after{
  border: none;
}
.item-box {
  height: 50px;
  background-color: #FFFFFF;
}
.item-box button {
  width: 25%;
  height: 100%;
  border-radius: 0px;
  line-height: 50px;
  text-align: center;
  color: #333;
  font-size: 14px;
  background-color: #FFFFFF;
}
.item-box-active{
  border-bottom: 2px solid #FF5E5E;
}

.item-item {
  margin-top: 10px;
  height: 125px;
  background-color: #fff;
  border-bottom: 1px solid #e5e5e5;
}

.item-item view{
  padding: 0 5px;
}

.item-option-box {
  width: 100vw;
}

.item-option-box button{
  height: 100%;
  border-radius: 0px;
  line-height: 50px;
  text-align: center;
  color: #2f6ce8;
  font-size: 16px;
  background-color: #FFFFFF;
}

</style>