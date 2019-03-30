<template>
	<div>
		<home-header></home-header>
		<home-swiper></home-swiper>
		<home-icons></home-icons>
		<home-recomend></home-recomend>
		<home-weekend></home-weekend>
	</div>	
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecomend from './components/Recomend'
import HomeWeekend from './components/Weekend'
export default {
	name:'Home',
	components:{
		HomeHeader,
		HomeSwiper,
		HomeIcons,
		HomeRecomend,
		HomeWeekend
	}
}
</script>

<style>
	
</style>
