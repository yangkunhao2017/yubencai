<template>
	<view>
		<view class="uni-flex uni-column title-box"
		:class="isUser?' title-box-user':'title-box-com'">
      <view class="uni-flex uni-row view-right">
        <view>
          <text class="option"><uni-icons type="gear-filled"></uni-icons>设置</text>
        </view>
      </view>
      <view class="uni-flex uni-row view-between account-info-box">
        <view class="uni-flex uni-row view-center">
          <view>
            <image class="message-list-box-logo" src="../../../static/logo.png" v-if="isUser"></image>
			<image class="message-list-box-logo" src="../../../static/logo.png" v-else="isUser"></image>
          </view>
          <view style="margin-left: 10px">
            <view>
              <text v-if="isUser">李聪</text>
			  <text style="color: #fff;" v-else="isUser">重庆梦比优斯网络科技有限公司</text>
            </view>
            <view>
              <text v-if="isUser">6年工作经验/26岁/本科</text>
			  <view class="uni-flex uni-row" style="color:orange;margin-top: 5px;" v-else="isUser">
			  <uni-icons type="phone-filled" color="orange"></uni-icons>
			 <text style="margin-left: 10px;"> 已认证</text>
			  </view>
            </view>
          </view>
        </view>
        <view class="clock" v-if="isUser">
          <text ><uni-icons type="map-pin-ellipse" > </uni-icons>打卡</text>
        </view>
      </view>
    </view>
    <view class="option-box uni-flex uni-row view-vertical-center" v-if="isUser">
      <view class="bg uni-flex uni-row">
        <view class="item">
          <view class="uni-flex uni-column view-center">
            <image src="../../../static/logo.png" ></image>
            <text>预览简历</text>
          </view>
        </view>
        <view class="item">
          <view class="uni-flex uni-column view-center">
            <image src="../../../static/logo.png" ></image>
            <text>编辑简历</text>
          </view>
        </view>
        <view class="item">
          <view class="uni-flex uni-column view-center">
            <image src="../../../static/logo.png" ></image>
            <text>投递简历</text>
          </view>
        </view>
        <view class="item">
          <view class="uni-flex uni-column view-center">
            <image src="../../../static/logo.png" ></image>
            <text>谁看过我</text>
          </view>
        </view>
      </view>
    </view>
	<view class="option-box uni-flex uni-row view-vertical-center" v-else="isUser">
	  <view class="bg uni-flex uni-row">
	    <view class="item">
	      <view class="uni-flex uni-column view-center">
	        <image src="../../../static/logo.png" ></image>
	        <text>财务管理</text>
	      </view>
	    </view>
	    <view class="item">
	      <view class="uni-flex uni-column view-center">
	        <image src="../../../static/logo.png" ></image>
	        <text>职位管理</text>
	      </view>
	    </view>
	    <view class="item">
	      <view class="uni-flex uni-column view-center">
	        <image src="../../../static/logo.png" ></image>
	        <text>邀约记录</text>
	      </view>
	    </view>
	    <view class="item">
	      <view class="uni-flex uni-column view-center">
	        <image src="../../../static/logo.png" ></image>
	        <text>人力资源</text>
	      </view>
	    </view>
	  </view>
	</view>
	<view style="border-bottom: 10px solid #EFEFF0FF;"></view>
    <view class="list-box" v-if="isUser">
      <uni-list>
        <uni-list-item  title="我的钱包" :to="`../my-center/my-wallet`" thumb="../../static/logo.png" thumb-size="lg" showArrow />
        <uni-list-item title="我的合同" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
        <uni-list-item title="我的足迹" :to="`../my-center/my-footprint`" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
        <uni-list-item title="求职意向" :to="`../my-center/job-wanted`" thumb="../../static/logo.png" thumb-size="lg" showArrow rightText="默认职位"/>
      </uni-list>
      <uni-list>
        <uni-list-item title="我的部门" :to="`../my-center/department`" thumb="../../static/logo.png" thumb-size="lg" showArrow rightText="暂未加入"/>
        <uni-list-item title="我要请假" :to="`../my-center/leave/leave`" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
        <uni-list-item title="我要报销" :to="`../my-center/reimbursement`" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
      </uni-list>
      <uni-list>
        <uni-list-item title="意见反馈" :to="`../my-center/feedback`" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
        <uni-list-item title="退出登录" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
      </uni-list>
    </view>
	<view class="list-box" v-else="isUser">
	  <uni-list>
	    <uni-list-item  title="企业钱包" :to="`../my-center/my-wallet`" thumb="../../static/logo.png" thumb-size="lg" showArrow />
	    <uni-list-item title="部门管理" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
	    <uni-list-item title="审批管理" :to="`../my-center/my-footprint`" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
	    <uni-list-item title="员工合同" :to="`../my-center/job-wanted`" thumb="../../static/logo.png" thumb-size="lg" showArrow />
	    <uni-list-item title="员工考勤" :to="`../my-center/department`" thumb="../../static/logo.png" thumb-size="lg" showArrow />
	    <uni-list-item title="企业认证" :to="`../my-center/leave/leave`" thumb="../../static/logo.png" thumb-size="lg" showArrow rightText="未认证"/>
	    <uni-list-item title="意见反馈" :to="`../my-center/reimbursement`" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
	    <uni-list-item title="退出登录" thumb="../../static/logo.png" thumb-size="lg" showArrow/>
	  </uni-list>
	</view>
    <view class="bottom">

    </view>
	</view>
</template>

<script>
  import UniSection from "../../components/uni-section/uni-section";
  export default {
    components: {UniSection},
    data() {
			return {
				isUser:false,
			}
		},
		methods: {
			
		}
	}
</script>

<style>

/*去掉按钮边框*/
button:after{
  border: none;
}

.title-box{
  height: 150px;
  
  display: flex;
  justify-content: space-between;
}
.title-box-com {
	background: #fc4039;
}
.title-boox-user {
	background: #2f6ce8;
}
.title-box .option{
  color: #fff;
  font-size: 20px;
}

.title-box .clock{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 80px;
  height: 30px;
  border-radius: 15px 0 0 15px;
  background: #faa339;
  color: #ffffff;
  font-size: 18px;
}

.account-info-box {
  margin-bottom: 30px;
}

.account-info-box image{
  width: 50px;
  height: 50px;
  border-radius: 50%;
}

.option-box {
  background-color: #FFFFFF;
  height: 80px;
}

.option-box .bg{
  background-color: #FFFFFF;
  height: 100%;
  width: 90%;
  margin-top:-40px;
  border-radius: 10px;
  box-shadow: 0 0 5px #000000;
}

.option-box .bg .item{
  width: 25%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.option-box .bg .item image{
  width: 50px;
  height: 50px;
  border-radius: 0%;
}

.list-box {
  background-color: #f4f4f5;
}

.list-box .uni-list{
  margin-bottom: 10px;
}

.bottom {
  height: 60px;
  background-color: #f4f4f5;
}
</style>
