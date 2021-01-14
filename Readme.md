
## 前言
绝对定位弹框，自定义弹框内容

## 有疑问
微信搜索“慢慢向好”小程序，找客服反馈，相应问题。
				  

## 素材
[图片资源](https://pixabay.com)
 
## 开始使用
下载源码解压，复制`/components` 下的组件至项目根目录的 `/components` 文件夹下


页面`index.vue` 引入 `ay-dropdown` 组件
```
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
```


页面`index.vue` 引入关键标签
```
<view class="cf-hengStart">
			<view style="text-align: center;">请点击选择</view>
			<dropdown :filterData='filterData'  @onSelected='onSelected'
			 :themeColor="themeColor"></dropdown>
				
		</view>
```


页面`index.vue` 引入背景色
```
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
```


## 参考
[参考插件1](https://ext.dcloud.net.cn/plugin?id=3615)
[参考插件2](https://ext.dcloud.net.cn/plugin?id=2315)
 