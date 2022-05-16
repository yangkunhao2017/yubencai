<template>
	<view>
    <view class="uni-flex uni-column job-info-title-box">
      <view class="job-info-title-box-title">
        JAVA开发工程师
      </view>
      <view class="job-info-title-box-requirement">
        <text style="color: #dd6e16">9k~15K</text>
        <text>/重庆大渡口区</text>
        <text>/2年及以上</text>
        <text>/学历不限</text>
      </view>
      <view class="job-info-title-box-welfare">
        职位福利：五险一金，餐补，年终奖，绩效奖金，岗位晋升
      </view>
      <view class="uni-flex uni-row job-info-company-box">
        <view>
          <image class="company-box-logo" src="../../../static/logo.png" ></image>
        </view>
        <view class="company-box-info">
          <view>
            <text class="company-box-name">拉勾网</text>
          </view>
          <view class="company-box-desc">
            <text>50人以下</text>
            <text>/互联网</text>
            <text>/软件开发</text>
            <text>/游戏开发</text>
          </view>
        </view>
      </view>
    </view>
    <view>
      <view>
        <view class="job-info-content-box-title">
          职位描述
        </view>
        <view class="uni-flex uni-column job-info-content-box-content">
          <text>岗位职责</text>
          <text>1、负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发</text>
          <text>2、负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发</text>
          <text>3、负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发，负责软件项目的开发</text>
        </view>
      </view>
    </view>
    <view class="uni-flex uni-row view-bottom">
      <button style="width: 20vw;font-size: 15px;background-color: #FFFFFF;border-radius: 0px;">打电话</button>
      <button style="width: 20vw;font-size: 15px;background-color: #FFFFFF;border-radius: 0px;">打招呼</button>
      <button style="width: 60vw;font-size: 15px;background-color: #1678ff;color: #ffffff;border-radius: 0px;">投递简历</button>
    </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

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

.job-info-title-box {
  padding: 10px;
  background: #fff;
  border-bottom: 1px solid #e5e5e5;
}

.job-info-title-box-title {
  font-size: 18px;
  color: #333;
}

.job-info-title-box-requirement {
  font-size: 14px;
  color: #2d2d2e;
  margin-top: 5px;
}

.job-info-title-box-welfare {
  font-size: 12px;
  color: #9a9a9b;
  margin-top: 5px;
}

.job-info-company-box {
  margin-top: 15px;
  font-size: 12px;
  color: #9a9a9b;
}

.company-box-logo {
  width: 50px;
  height: 50px;
  border-radius: 5px;
}

.company-box-info {
  margin-left: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.company-box-name {
  font-size: 24px;
  color: #000000;
}

.company-box-desc {
  font-size: 16px;
}

.job-info-content-box-title {
  font-size: 20px;
  font-weight: bold;
}

.job-info-content-box-content {
  font-size: 16px;
}

.view-bottom {
  /* #ifndef APP-NVUE */
  display: flex;
  /* #endif */
  position: fixed;
  left: 0;
  right: 0;
  /* #ifdef H5 */
  left: var(--window-left);
  right: var(--window-right);
  /* #endif */
  bottom: 0;
  background-color: #ffffff;
}
</style>
