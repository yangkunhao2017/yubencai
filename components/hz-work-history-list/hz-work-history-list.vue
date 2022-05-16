<template>
	<view>
    <view class="want-info">
      <view class="uni-flex uni-column">
        <text class="title">求职意向</text>
        <view>
          <text class="key">期望职位</text>
          <text v-if="isShow==true" class="value">java开发工程师</text>
          <uni-easyinput v-if="isShow==false" class="value">java开发工程师</uni-easyinput>
        </view>
        <view>
          <text class="key">期望行业</text>
          <text v-if="isShow==true" class="value">java开发工程师</text>
          <uni-easyinput v-if="isShow==false" class="value">java开发工程师</uni-easyinput>
        </view>
        <view>
          <text class="key">期望地点</text>
          <text v-if="isShow==true" class="value">java开发工程师</text>
          <uni-easyinput v-if="isShow==false" class="value">java开发工程师</uni-easyinput>
        </view>
        <view>
          <text class="key">期望薪资</text>
          <text v-if="isShow==true" class="value">java开发工程师</text>
          <uni-easyinput v-if="isShow==false" class="value">java开发工程师</uni-easyinput>
        </view>
      </view>
    </view>
    <view class="work-history" v-for="i in historyList">
      <view class="title">
        <text>工作/实习经历</text>
      </view>
      <view class="uni-flex uni-row">
        <view>
          <uni-icons type="locked-filled"></uni-icons>
        </view>
        <view class="uni-flex uni-column">
          <view>
            <text class="time">2018-2 至 今 （3年8个月)</text>
          </view>
          <view>
            <text class="job">{{i.jobName}}</text>
          </view>
          <view>
            <text class="company">重庆梦比优斯网络科技有限公司</text>
          </view>
          <view>
            <text class="company-info">50人以下/互联网/游戏开发</text>
          </view>
          <view class="uni-flex uni-column work-info">
            <text v-if="isShow==true">1.大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦在\n2.大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦在\n3.大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦在\n4.大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦大厦在</text>
            <uni-easyinput v-if="isShow==false"></uni-easyinput>
          </view>
        </view>
      </view>
    </view>
	</view>
</template>

<script>
  export default {
		name:"hz-work-history-list",
    data() {
			return {
				
			};
		},
		props:{
			historyList:{
        type:Array,
        default:()=> {
          return [];
        },
      },
      isShow:{
        type:Boolean,
        default:true,
      }
		},
    methods: {
    },
	}
</script>

<style>

.want-info {
  margin-top: 10px;
  padding: 10px;
  background-color: #ffffff;
}

.want-info .title{
  font-size: 18px;
  color: #333333;
}

.want-info .key{
  font-size: 14px;
  color: #999999;
}

.want-info .value{
  font-size: 14px;
  color: #333333;
  margin-left: 10px;
}


.work-history {
  margin-top: 10px;
  padding: 10px;
  background-color: #ffffff;
}

.work-history .title{
  font-size: 18px;
  color: #333333;
}

.work-history .time{
  font-size: 14px;
  color: #000000;
}

.work-history .job{
  font-size: 14px;
  font-weight: bold;
  color: #000000;
}

.work-history .company{
  font-size: 14px;
  color: #000000;
}

.work-history .company-info{
  font-size: 14px;
  color: #999999;
}

.work-history .work-info{
  margin-top: 10px;
  font-size: 14px;
  color: #999999;
}

.work-history text{
  word-break:break-all;
}
</style>