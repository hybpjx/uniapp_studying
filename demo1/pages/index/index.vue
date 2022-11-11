<template>
	<view class="out">
		
		<!-- 图片 -->
		
		<image src="/static/images/1.png" mode="" class="myimg"></image>
		<!-- 以宽度位基准 -->
		<image src="/static/images/2.png" mode="heightFix" class="mypic" ></image>
		<!-- <img src="/static/images/1.png" alt=""> 会有一个默认的宽高 -->
		
		<view class="box">hello</view>
		<view class="block">
		</view>

		<icon type="success" size="26" />
		<icon type="warn" size="26" />

		<view>uniapp</view>
		<view>web 前端开发</view>

		<text user-select selectable> node.js json</text>
		<!-- 转义 自动解码 -->
		<text space="ensp" decode> vue &gt; js</text>
		<!-- 上下 xy 都支持滑动 -->
		<scroll-view class="scroll" scroll-x scroll-y>
			<view class="group">
				<view class="item">
					111
				</view>

				<view class="item">
					111
				</view>

				<view class="item">
					111
				</view>

				<view class="item">
					111
				</view>

			</view>
		</scroll-view>

	
		<!-- 					衔接滑动 自动切换   切换时间间隔   滑动动画时长 	 显示面板指示点  	指示点颜色				选中的指示点颜色-->
		<swiper  class="swiper" circular autoplay interval="3000" duration="200" indicator-dots indicator-color="#fff" indicator-active-color="green">
			<swiper-item>
				<!-- aspectFill 将短边显示出来 -->
				<image src="/static/images/1.png" mode="aspectFill"></image>
			</swiper-item>
			<swiper-item>
				<image src="/static/images/2.png" mode="aspectFill"></image>
			</swiper-item>
			<swiper-item>
				<image src="/static/images/3.png" mode="aspectFill"></image>
			</swiper-item>
		</swiper>
		
		
		<view class="" style="height: 450rpx;"></view>
			
		<!-- autoplay 允许自动播放 duration="20" 截取20s  initial-time="20" 从20s开始播放 -->
		<video src="../../static/images/mda-nka8cbj5veh1sp0p.mp4" :controls="false">
			
		</video>
		
		<!-- 按钮标签 -->
		<button type="warn" size="default">确认提交</button>
		<button type="primary" size="mini" loading>确认提交</button>
		
		<!-- input标签 -->
		<input type="password">
		
		
		<!-- 一旦加了tarBar 就跳转不了 open-type就 跳转不了了 -->
		<!-- 这个时候只有reLaunch可以跳转 -->
		<navigator url="/pages/list/list" open-type="reLaunch">新闻列表</navigator>
		
		<navigator url="/pages/list/list" open-type="reLaunch">
			<image src="../../static/images/1.png" mode=""></image>
		</navigator>
		
		<!-- open-type="redirect" 等于新打开了一个页面 -->
		<navigator url="/pages/about/about" open-type="reLaunch">关于我</navigator>
		
		
		
	</view>

</template>

<script>
	export default {
		data() {
			return {}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	
	.myimg{
		width:300rpx;
		// height: 240rpx;
	}
	
	.mypic{
		
	}
	
	.box {
		height: 200px;
		width: 200px;
		background-color: pink;

		.block {
			width: 750rpx;
			height: 750rpx;
			background-color: green;
		}
	}

	.scroll {
		border: 1px solid red;
		box-sizing: border-box;
		height: 100rpx;

		.group {
			// 不换行
			white-space: nowrap;
			.item {
				width: 220rpx;
				height: 220rpx;
				background: royalblue;
				// 行级块元素
				display: inline-block;
				margin-right: 10rpx;
			}
		}
	}
	
	.swiper {
		// swiper有默认的高度 所以要修改
		height: 500rpx;
		margin-top: 40rpx;
		swiper-item{
			
			padding: 20rpx;
			// 内填充
			box-sizing: border-box;
			
			image{
				width: 100%;
				height: 500rpx;
			}
		}
	}
	
</style>
