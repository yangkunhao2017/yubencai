<template>
	<view style="background-color: #f6f6f6;">
    <button v-if="isEdit==false" type="primary" @click="changeEdit()">编辑</button>
    <button v-if="isEdit==true" type="primary" @click="changeEdit()">保存</button>
		<view class="my-info uni-flex uni-column">
      <view class="uni-flex uni-row">
        <view>
          <image src="../../../../static/logo.png"></image>
        </view>
        <view>
          <view>
            <text>李聪</text>
          </view>
          <view>男·26岁·本科·6年工作经验·172cm</view>
        </view>
      </view>
      <view>
        <text><uni-icons type="locked-filled"></uni-icons>重庆市-大渡口区-松青大道</text>
      </view>
      <view class="uni-flex uni-row view-between">
        <text><uni-icons type="locked-filled"></uni-icons>17700210028</text>
        <text><uni-icons type="locked-filled"></uni-icons>lichong0220@163.com</text>
      </view>
    </view>

    <view>
      <hz-work-history-list :history-list="historyList" :is-show="!isEdit"></hz-work-history-list>
    </view>
	</view>
</template>

<script>
	import HzWorkHistoryList from "../../../../components/hz-work-history-list/hz-work-history-list";
  export default {
    components: {HzWorkHistoryList},
    data() {
			return {
        isEdit: false,
				historyList: [{
          jobName:'java开发工程师',
        }]
			}
		},
		methods: {
			changeEdit() {
        if(this.isEdit) {
          // 保存
        } else {
          // 编辑
        }
        this.isEdit = !this.isEdit;
      }
		}
	}
</script>

<style>
.my-info {
  height: 100px;
  background-color: #ffffff;
  padding: 10px;
}

.my-info image{
  width: 50px;
  height: 50px;
  border-radius: 50%;
}


</style>
