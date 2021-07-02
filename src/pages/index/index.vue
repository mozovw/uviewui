<template>
	<view>
		<u-navbar back-text="返回" :is-back="false" title="小工具"></u-navbar>
		<view class="content">
			<!-- 正文内容 -->
			<u-grid :col="3" :border="false">  
				<u-grid-item @click="toNext('/pages/account/index')">       
					<u-icon  name="photo" :size="46"></u-icon>
					<view class="grid-text">图片</view>
					</u-grid-item>   
				<u-grid-item>
					<image src="/static/image/icon/hot5.png" class="badge-icon"></image>
					<u-icon name="lock" :size="46"></u-icon>
					<view class="grid-text">锁头</view>
				</u-grid-item>
				<u-grid-item>
					<u-icon name="hourglass" :size="46"></u-icon>
					<view class="grid-text">沙漏</view>
				</u-grid-item>
			</u-grid>
		</view>
		<!-- 与包裹页面所有内容的元素u-page同级，且在它的下方 -->
		<u-tabbar v-model="current" :list="list" :mid-button="true" :before-switch="beforeSwitch"></u-tabbar>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
						iconPath: "home",
						selectedIconPath: "home-fill",
						text: '首页',
						customIcon: false,
					},
					{
						iconPath: "photo",
						selectedIconPath: "photo-fill",
						text: '放映厅',
						customIcon: false,
					},
					{
						iconPath: "play-right",
						selectedIconPath: "play-right-fill",
						text: '直播',
						customIcon: false,
					},
					{
						iconPath: "account",
						selectedIconPath: "account-fill",
						text: '我的',
						customIcon: false,
					},
				],
				current: 0
			}
		},
		methods:{
			toNext(url) {
				if (url == 'jqqd') {
					this.$u.toast('敬请期待！')
				}else{
					this.$u.route(url)
				}
			},
			beforeSwitch(index) {
				this.$u.route("/pages/account/index")
			}
		}
	}
</script>

<style scoped lang="scss">
	.content {
		padding: 2%;
	}
	.badge-icon {
		position: absolute;
		top: 14rpx;
		right: 40rpx;
		width: 30rpx;
		height: 30rpx;
	}
	
	.grid-text {
		font-size: 28rpx;
		margin-top: 4rpx;
		color: $u-type-info;
	}
</style>