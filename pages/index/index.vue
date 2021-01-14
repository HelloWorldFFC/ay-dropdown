<template>
	<view class="content">
		<view class="cf-hengStart">
			<view style="text-align: center;">请点击选择</view>
			<dropdown :filterData='filterData'  @onSelected='onSelected'
			 :themeColor="themeColor"></dropdown>
				
		</view>
		<view class="cf-hengStart">
			<view style="text-align: center;">请点击选择</view>
			<dropdown :filterData='filterData'  @onSelected='onSelected'
			 :themeColor="themeColor"></dropdown>
				
		</view>
		<view class="cf-hengStart">
			<view style="text-align: center;">请点击选择</view>
			<dropdown :filterData='filterData'  @onSelected='onSelected'
			 :themeColor="themeColor"></dropdown>
				
		</view>
		<view class="cf-hengStart">
			<view style="text-align: center;">请点击选择</view>
			<dropdown :filterData='filterData'  @onSelected='onSelected'
			 :themeColor="themeColor"></dropdown>
				
		</view>
	</view>
</template>

<script>
	import dropdown from '@/components/ay-dropdown/ay-dropdown.vue'
	export default {
		components: {
			dropdown,

		},
		data() {
			return {
				themeColor: '#33CCCC',
				filterData: [
					[{
						text: '<1折',
						value: '0.9'
					}, {
						text: '1-2折',
						value: '1-2'
					}],
				],
			}
		},
		onLoad() {
			let that = this;

		},

		methods: {
			onSelected(res) {
				//[[{"text":"<1折","value":"0.9","select":true}],[{"text":"距离优先","value":"距离优先","select":true}]]
				// console.log('res  ' + JSON.stringify(res))
				// console.log('res  ' + JSON.stringify(res[0]))
				// console.log('res  ' + JSON.stringify(res[0][0].value))
				let that = this;
				let one = res[0][0].value;
				console.log(' one ' + one);
			},

		}
	}
</script>

<style>
	page {
		background-color: #f2f2f2;
	}
	.cf-hengStart {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		width: 100%;
	}
</style>
