<template>
	<view>
		<view class="bottom-box">
			<view class="uni-flex uni-row ">
				<view class="uni-flex title-text view-vertical-center">
				<text >审批人</text>
				</view>
			</view>
		</view>
		<view style="border-bottom: 12px solid #ececec;"></view>
		<view class="uni-flex uni-row" style="margin-top: 10px;">
		<view class="uni-flex uni-row view-center" style="margin-left: 10px;margin: 10px;">
			<text>选择审批人</text>
		</view>
		</view>
		<view style="border-bottom: 12px solid #ececec;"></view>
		<uni-collapse>
		<uni-collapse-item title="市场部(3)">
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="董事长"></uni-list-item>
				<view class="uni-px-5 uni-pb-5" style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio1" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="管理"></uni-list-item>
				<view class="uni-px-5 uni-pb-5 " style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio2" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				<view class="uni-px-5 uni-pb-5" style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio3" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
		</uni-collapse-item>
		<uni-collapse-item title="财务部(3)">
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="财务总监"></uni-list-item>
				<view class="uni-px-5 uni-pb-5" style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio4" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="财务主管"></uni-list-item>
				<view class="uni-px-5 uni-pb-5" style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio5" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				<view class="uni-px-5 uni-pb-5" style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio6" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
		</uni-collapse-item>
		<uni-collapse-item title="技术开发部(3)">
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="技术总监"></uni-list-item>
				<view class="uni-px-5 uni-pb-5" style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio7" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="技术主管"></uni-list-item>
				<view class="uni-px-5 uni-pb-5" style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio8" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row view-between" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				<view class="uni-px-5 uni-pb-5" style="margin-top: 10px;">
					<uni-data-checkbox  v-model="radio9" :localdata="sex"></uni-data-checkbox>
				</view>
				</view>
			</uni-list>
		</uni-collapse-item>
		</uni-collapse>
		<view style="border-bottom: 250px solid #ececec;"></view>
		<view class="uni-flex uni-row view-between view-center" style="margin-top: 10px;margin-bottom: 10px;">
			<text style="color: #0c7cf9;margin-left: 10px;">已选择: 1人</text>
			<button class="button-of">确定</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				radio1: 1,
				radio2: 1,
				radio3: 1,
				radio4: 1,
				radio5: 1,
				radio6: 1,
				radio7: 1,
				radio8: 1,
				radio9: 1,
				sex:[{
					value:0
				}],
			}
			
		},
		onLoad() {},
		onReady() {},
		methods: {
			
			}
	}
</script>

<style>
	.bottom-box {
		width: 100%;
	  height: 80px;
	  background-color: #0c7cf9;
	}
	.title-text {
		color: #FFFFFF;
		font-size: 18px;
		font-family: sans-serif;
		margin-top: 20px;
	}



	.text-leave {
		color: #c4c3c3;
	}

	.bottom-shi {
	  height: 150px;
	}
	.job-logo{
		width: 35px;
		height: 35px;
	}
	.text {
		font-size: 12px;
		color: #666;
		margin-top: 15px;
	}
	
	.uni-px-5 {
		padding-left: 10px;
		padding-right: 10px;
	}
	
	.uni-pb-5 {
		padding-bottom: 10px;
	}
	.button-of {
		background-color:#0c7cf9 ;
		color: #FFFFFF;
		line-height: 45px;
		width:200px;
		margin-left: 80px;
	}
</style>
