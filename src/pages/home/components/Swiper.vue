<template>
<div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList"
					:key='item.id' 		>
	<img class="swiper-img" :src='item.imgUrl'>
    </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
 </div>
</template>

<script>
export default {
	name:"HomeSwiper",
	data () {
		return {
			swiperOption:{
				pagination: '.swiper-pagination',
				loop:true
			},
			swiperList:[{
				id:'0001',
				imgUrl:'http://img1.qunarzz.com/piao/fusion/1807/ec/278a34afb59a0d02.jpg_750x200_3292a705.jpg'
			},{
				id:'0002',
				imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/278a88f18f1523eec8c52f650522be68.jpg_750x200_bc365244.jpg'
			}]
		}
	}
}	
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active{
	background: #fff }
	.wrapper
		width: 100%
		height: 0
		overflow:hidden
		padding-bottom:26.5%
		background: #ccc
		.swiper-img
			width: 100%
</style>