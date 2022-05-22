<template>
	<view>
		<view class="bottom-box">
			<view class="uni-flex uni-row ">
				<view class="uni-flex title-text view-vertical-center">
				<text >我的部门</text>
				</view>
			</view>
		</view>
		<view style="border-bottom: 12px solid #ececec;"></view>
		<view class="uni-flex uni-row" style="margin-top: 10px;">
		<view class="uni-flex uni-row view-center" style="margin-left: 10px;margin: 10px;">
			<image class="job-logo" src="../../static/logo.png" mode="scaleToFill"></image>
			<text>重庆梦比优斯网络科技有限公司</text>
		</view>
		</view>
		<view style="border-bottom: 12px solid #ececec;"></view>
		<uni-collapse>
		<uni-collapse-item title="市场部(3)">
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="董事长"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="管理"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				</view>
			</uni-list>
		</uni-collapse-item>
		<uni-collapse-item title="财务部(3)">
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="财务总监"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="财务主管"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				</view>
			</uni-list>
		</uni-collapse-item>
		<uni-collapse-item title="技术开发部(3)">
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="技术总监"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="技术主管"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				</view>
			</uni-list>
		</uni-collapse-item>
		</uni-collapse>
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
	.job-logo{
		width: 35px;
		height: 35px;
	}
	.content {
		padding: 15px;
	}
	
	.text {
		font-size: 14px;
		color: #666;
		line-height: 20px;
	}
</style>
