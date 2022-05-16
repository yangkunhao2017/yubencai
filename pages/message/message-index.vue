<template>
	<view>
		<view class="message-title-box uni-flex uni-column">
      <view class="uni-flex message-title-box-title">
        <text class="message-title-box-title-text">消息通知</text>
      </view>
      <view class="message-title-box-select uni-flex uni-row">
        <view class="uni-flex uni-row">
          <text :class="showLable!=0?'message-title-box-select-item':'message-title-box-select-item-active'" @click="changeShowLableIndex(0)">消息列表</text>
          <text :class="showLable!=1?'message-title-box-select-item':'message-title-box-select-item-active'" @click="changeShowLableIndex(1)">我的投递</text>
          <text :class="showLable!=2?'message-title-box-select-item':'message-title-box-select-item-active'" @click="changeShowLableIndex(2)">企业消息</text>
        </view>
      </view>
    </view>
    <hz-message-list v-if="showLable==0"></hz-message-list>
    <hz-message-send-list v-if="showLable==1"></hz-message-send-list>
    <hz-option-message-list v-if="showLable==2"></hz-option-message-list>
    <view style="height: 50px"></view>
	</view>
</template>

<script>
  import HzMessageList from "../../components/hz-message-list/hz-message-list";
  import HzMessageSendList from "../../components/hz-message-send-list/hz-message-send-list";
  import HzOptionMessageList from "../../components/hz-option-message-list/hz-option-message-list";
  export default {
    components: {HzOptionMessageList, HzMessageSendList, HzMessageList},
    data() {
			return {
				showLable:0,
			}
		},
		methods: {
			changeShowLableIndex(e){
        this.showLable = e;
      }
		}
	}
</script>

<style>
/*去掉按钮边框*/
button:after{
  border: none;
}
.message-title-box {
  height: 100px;
  background-color: #1678ff;
  border-bottom: 1px solid #e5e5e5;
}

.message-title-box-title {
  color: #fff;
  margin-top: 20px;
  -webkit-justify-content: center;
  justify-content: center;
}

.message-title-box-select {
  margin-top: 10px;
  -webkit-flex: 1;
  flex: 1;
  -webkit-align-items: flex-end;
  align-items: flex-end;
}

.message-title-box-title-text {
  font-size: 24px;
  font-weight: bold;
}

.message-title-box-select-item {
  font-size: 18px;
  color: #e5e5e5;
  margin:10px;
}

.message-title-box-select-item-active {
  font-size: 20px;
  font-weight: bold;
  color: #fff;
  margin:10px;
}

.bottom {
  height: 60px;
  background-color: #f6f6f6;
}

</style>
