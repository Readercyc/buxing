<template>
	<scroll-view scroll-x class="nav">
		<view class="flex text-center bg-red light navBar">
			<view class="cu-item flex-sub tab" :class="index==TabCur?'bg-red':''" v-for="(item,index) in navlist" :key="index" @tap="tabSelect($event)" :data-id="index">
				{{item}}
			</view>
		</view>
		<search></search>
		<view class="cu-card article" v-if="TabCur==0">
			<find-cloth  v-for="(item,index) in findClothList"
				:title="item.title"
				:img="item.img"
				:price="item.price"
				:time="item.time"
				:type="item.type">
			</find-cloth>
		</view>
		<view class="cu-card article" v-if="TabCur==1">
			<new-cloth v-for="(item,index) in newClothList"
				:title="item.title"
				:img="item.img"
				:price="item.price"
				:time="item.time"
				:attention="item.attention"
				:appreciate="item.appreciate"
				:message="item.message">
			</new-cloth>
		</view>
		<view class="cu-card case" v-if="TabCur==2">
			<store v-for="(item,index) in storeList"
				:name="item.name"
				:img="item.img"
				:avatar="item.avatar"
				:address="item.address"
				:attention="item.attention"
				:appreciate="item.appreciate"
				:message="item.message"
				:type="item.type">
			</store>
		</view>
		<view class="cu-card dynamic" v-if="TabCur==3">
			<notice v-for="(item,index) in noticeList"
				:title="item.title"
				:time="item.time"
				:img="item.img"
				:editor="item.editor">
			</notice>
		</view>
	</scroll-view>
</template>

<script>
	import findCloth from './findCloth.vue'
	import newCloth from './newCloth.vue'
	import store from './store.vue'
	import notice from './notice.vue'
	import search from './search.vue'
	export default{
		components:{
			findCloth,
			newCloth,
			store,
			notice,
			search
		},
		data(){
			return {
				navlist:['找布','新布','店铺','通知'],
				findClothList:[
					{id:1,title:'请问谁这种布有黄色的吗',img:'../../static/cloth/0-2.jpg',price:'40-50元/斤',time:'2020-3-31',type:'蕾丝'},
					{id:2,title:'请问谁这种布涤纶的谁有',img:'../../static/cloth/1-2.jpg',price:'7元/米',time:'2020-3-31',type:'蕾丝'},
					{id:3,title:'请问谁家有这种布的吗',img:'../../static/cloth/2-2.jpg',price:'无',time:'2020-3-31',type:'网布'},
					{id:4,title:'请问谁家有现货的小梅花红色',img:'../../static/cloth/3-2.jpg',price:'45/斤',time:'2020-3-31',type:'蕾丝'},
					{id:5,title:'急！谁家的工厂现在可以做星星花',img:'../../static/cloth/4-2.jpg',price:'38元/磅',time:'2020-3-31',type:'蕾丝'},
				],
				newClothList:[
					{id:6,title:'大梅花涤纶款现在开卖了！',img:'../../static/cloth/5-2.jpg',price:'40/斤',time:'2020-3-31',attention:"10",appreciate:"20",message:"30"},
					{id:7,title:'D50,植绒D48刚到货',img:'../../static/cloth/6-2.jpg',price:'40-50/斤',time:'2020-3-31',attention:"10",appreciate:"20",message:"30"},
					{id:8,title:'质量超棒的韩国弹力网',img:'../../static/cloth/7-2.jpg',price:'7元/米',time:'2020-3-31',attention:"10",appreciate:"20",message:"30"},
					{id:9,title:'新到的锦氨纶网布，一共64种颜色！',img:'../../static/cloth/8-2.jpg',price:'35/斤',time:'2020-3-31',attention:"10",appreciate:"20",message:"30"},
					{id:10,title:'美国进口的美洲网，不要错过！',img:'../../static/cloth/9-2.jpg',price:'40-50/斤',time:'2020-3-31',attention:"10",appreciate:"20",message:"30"},
				],
				storeList:[
					{id:11,name:'佳鑫',address:'长江纺织城南二街A50',avatar:'../../static/store/logojiaxin.png',img:'../../static/store/Bannerjiaxin.png',attention:"10",appreciate:"20",message:"30",type:"网布、蕾丝"},
				],
				noticeList:[
					{id:12,title:'因疫情原因导致的租赁费用补偿的相关通知',time:'2020-3-31',img:"",editor:'中大市场管理处'}
				],
				TabCur: 0,
				scrollLeft: 0
			}
		},
		methods:{
			tabSelect(e) {
				this.TabCur = e.currentTarget.dataset.id;
				//传参到后端，获取对应的文章列表
			}
		}
	}
</script>

<style scoped>
	.nav{
		padding-bottom: 50px;
	}
	.navBar{
		position: fixed;
		z-index: 999;
		top: 0px;
		width: 100%;
	}
	.tab{
		font-weight: bold;
		transition: 0.3s;
		margin: 0;
		border: 0!important;
	}
	.article,.case,.dynamic{
		width: 100%;
		margin-top: 100px;
		display: flex;
		flex-wrap: wrap;
	}
</style>
