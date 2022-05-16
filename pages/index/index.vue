<template>
	<view style="background: #f6f6f6;">
		<view class="title-box uni-flex uni-column view-vertical-center">
			<view class="uni-flex uni-row">
				<view class="uni-flex uni-row view-center" style="width: 20vw;">
					<uni-icons type="flag-filled"></uni-icons>
					<text style="font-size: 15px;font-weight: bold;color: #ffffff;">重庆市</text>
				</view>
				<view class="uni-flex view-vertical-center" style="width: 60vw;">
					<image class="title-logo" src="../../static/logo.png" mode="scaleToFill"></image>
				</view>
				<view class="uni-flex view-center" style="width: 20vw;">
				</view>
			</view>
			<view>
				<view class="uni-flex uni-row input-box view-center">
					<view style="margin-left: 10px;">
						<uni-icons type="phone-filled"></uni-icons>
					</view>
					<input class="input-input" placeholder="搜职位\公司" style="margin-left: 3px;"/>
					<view style="height: 20px;width: 2px;background: #000;margin-right: 10px;"></view>
					<text style="font-size: 18px;color: #ffffff;margin-right: 10px;">搜索</text>
				</view>
			</view>
		</view>
		<!-- 热门职位 -->
		<view class="hot-job-box">
			<view>
				<text style="margin-left: 10px;">热门职位</text>
			</view>
			<view class="uni-flex uni-row view-warp">
				<view class="hot-job-box-item uni-flex view-center" v-for="index in hotJob" @click="selectHotJob(index.id)">
					{{index.name!=null?index.name:'测试职位'}}
				</view>
			</view>
		</view>
		<!-- 筛选 -->
		<view>
			<view class="uni-flex uni-row" style="background-color: #ffffff;">
				<text class="screen-title">推荐</text>
				<text class="screen-title">最新</text>
			</view>
			<view class="uni-flex uni-row screen-box">
				<button class="screen-box-item" @click="showPopup('region')">地区<uni-icons type="bottom"/></button>
				<button class="screen-box-item" @click="showPopup('salary')">薪资<uni-icons type="bottom"/></button>
				<button class="screen-box-item" @click="showPopup('education')">学历<uni-icons type="bottom"/></button>
				<button class="screen-box-item" @click="showPopup('other')">其他<uni-icons type="bottom"/></button>
			</view>
		</view>
		<!-- 列表 -->
		<view>
			<view class="uni-flex uni-column job-list-box" v-for="index in 10">
				<view class="uni-flex uni-row view-between">
					<view style="margin-left: 10px;">
						<text class="job-list-title uni-ellipsis">java中级工程师</text>
					</view>
					<view class="job-list-treatment" style="margin-right: 10px;">
						<text>9K~15K</text>
					</view>
				</view>
				<view class="uni-flex uni-row" style="margin-top: 10px;">
					<view class="uni-flex view-center job-list-ticp" v-for="index in 4">
						ticp
					</view>
				</view>
				<view style="width: 100%;border-bottom: 1px dashed #EFEFF0FF;margin-top: 10px;">
				</view>
				<view class="uni-flex uni-row" style="margin-top: 10px;">
					<view style="margin-left: 10px;margin: 5px;">
						<image class="job-logo" src="../../static/logo.png" mode="scaleToFill"></image>
					</view>
					<view class="uni-flex uni-column" style="width: 50vw;margin: 5px;">
						<view class="uni-ellipsis-1">
							重庆梦比优斯网络科技有限公司
						</view>
						<view class="uni-ellipsis-1" style="color:#99999AFF;font-size: 14px;">
							50人以下·互联网、软件开发·氛围好
						</view>
					</view>
					<view style="margin: 5px;">
						<button class="job-list-button-send">投递简历</button>
					</view>
				</view>
			</view>
		</view>
		<uni-section></uni-section>
		<uni-section></uni-section>
	</view>
	
	
	<!-- 普通弹窗 -->
	<uni-popup ref="region" background-color="#fff">
		<view class="popup-content uni-flex uni-column">
			<view class="uni-flex uni-row">
				<view>
					<scroll-view  scroll-y="true" class="scroll-Y">
						<view class="scroll-view-item" v-for="index in 20">{{index}}</view>
					</scroll-view>
				</view>
				<view>
					<scroll-view  scroll-y="true" class="scroll-Y">
						<view class="scroll-view-item" v-for="index in 20">{{index}}</view>
					</scroll-view>
				</view>
				<view>
					<scroll-view  scroll-y="true" class="scroll-Y">
						<view class="scroll-view-item" v-for="index in 20">{{index}}</view>
					</scroll-view>
				</view>
			</view>
			<view>
				<button @click="closePopup('region')">确定</button>
			</view>
		</view>
	</uni-popup>
	<uni-popup ref="salary" background-color="#fff">
		<view class="popup-content uni-flex uni-column">
			<view>
				<uni-section title="最小薪资" type="line">
				      <uni-data-select
				        v-model="value"
				        :localdata="rangeMin"
				        @change="change"
				      ></uni-data-select>
				</uni-section>
			</view>
			<view>
				<uni-section title="最大薪资" type="line">
				      <uni-data-select
				        v-model="value"
				        :localdata="rangeMax"
				        @change="change"
				      ></uni-data-select>
				</uni-section>
			</view>
			<button @click="closePopup('salary')">确定</button>
		</view>
	</uni-popup>
	<uni-popup ref="education" background-color="#fff">
		<view class="popup-content">
			<uni-section title="学历" type="line">
			      <uni-data-select
			        v-model="value"
			        :localdata="education"
			        @change="change"
			      ></uni-data-select>
			</uni-section>
			<button @click="closePopup('education')">确定</button>
		</view>
	</uni-popup>
	<uni-popup ref="other" background-color="#fff">
		<view class="popup-content">
			其他
			<button @click="closePopup('other')">确定</button>
		</view>
	</uni-popup>
</template>

<script>
	export default {
		data() {
			return {
				hotJob:[{},{},{},{},{},{},{},{},{}],
				rangeMin: [
				  { value: 0, text: "1000" },
				  { value: 1, text: "2000" },
				  { value: 2, text: "3000" },
				],
				rangeMax: [
				  { value: 0, text: "2000" },
				  { value: 1, text: "3000" },
				  { value: 2, text: "4000" },
				],
				education: [
				  { value: 0, text: "小学" },
				  { value: 1, text: "初中" },
				  { value: 2, text: "高中/中专" },
				  { value: 3, text: "本科及以上" },
				],
			}
		},
		methods: {
			selectHotJob(e){
				console.log(e)
			},
			showPopup(e){
				if(e=='region'){
					this.$refs.region.open('left');
				}else if(e=='salary'){
					this.$refs.salary.open('left');
				}else if(e=='education'){
					this.$refs.education.open('left');
				}else if(e=='other'){
					this.$refs.other.open('left');
				}
				
			},
			closePopup(e){
				if(e=='region'){
					this.$refs.region.close();
				}else if(e=='salary'){
					this.$refs.salary.close();
				}else if(e=='education'){
					this.$refs.education.close();
				}else if(e=='other'){
					this.$refs.other.close();
				}
			}
		}
	}
</script>

<style>
	.title-box{
		height: 25vh;
		background: #55aaff;
	}
	.title-logo{
		width: 150px;
		height: 50px;
	}
	.input-box {
	    /* #ifndef APP-NVUE */
	    display: flex;
	    /* #endif */
	    padding: 10px 5px;
	    flex-direction: row;
	    flex-wrap: nowrap;
	    background-color: rgba(255, 255, 255, 0.1);
		margin-top: 30rpx;
		width: 90vw;
		border-radius: 5px;
	}
	.input-input {
	    height: 28px;
	    line-height: 28px;
	    font-size: 15px;
	    padding: 0px;
	    flex: 1;
		color: #ffffff;
		
	}
	.hot-job-box{
		margin-top: -20px;
		height: 180px;
		background: #ffffff;
		border-radius: 10px 10px 0px 0px;
		font-size: 25px;
	}
	.hot-job-box-item{
		width: 31vw;
		height: 40px;
		background: #e7f0ff;
		margin: 1vw;
		font-size: 14px;
		font-weight: bold;
	}
	.screen-box{
		background: #ffffff;
		border: 1px solid #f2f2f2;
	}
	.screen-title{
		font-size: 24px;
		margin: 10px;
		border-bottom: 5px solid #0c7cf9;
	}
	.screen-box-item{
		color: #919191;
		background: #ffffff;
		border: none;
	}
	.popup-content{
		width: 100vw;
	}
	.scroll-view-item {
		height: 100rpx;
		line-height: 100rpx;
		text-align: center;
		font-size: 36rpx;
	}
	.scroll-Y {
		width: 100px;
		height: 80vh;
	}
	.job-logo{
		width: 50px;
		height: 50px;
	}
	/*去掉按钮边框*/
	button:after{ border: none; }

  .job-list-box {
    background: #ffffff;
    margin-top: 10px;
  }

  .job-list-title {
    font-size: 24px;
  }

  .job-list-treatment {
    color: #dd6e16;
  }

  .job-list-ticp {
    width: 80px;
    height: 30px;
    background: #ECECEDFF;
    margin-left: 10px;
  }

  .job-list-button-send {
    background-color: #FFFFFF;
    color: #0c7cf9;
    border: 1px solid #0c7cf9;
  }
</style>
