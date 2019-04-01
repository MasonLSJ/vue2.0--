<template>
	<div class="list" ref="wrapper">
	<div>
		<div class="area">
			<div class="title border-topbottom">The current city</div>
			<div class="button-list">
				<div class="button-wraper">
					<div class="button button-bg">{{this.$store.state.city}}</div>
				</div>
			</div>
		</div>
		<div class="area">
			<div class="title border-topbottom">Hot city</div>
			<div class="button-list">
        	  <div
        	    class="button-wraper"
        	    v-for="item of hotCities"
        	    :key="item.id"
        	    @click='handleCityClick(item.name)'
        	  >
            <div class="button">{{item.name}}</div>
				</div>
			</div>
		</div>
      <div class="area"
           v-for="(item, key) of cities"
           :key="key"
           :ref="key"
      >
        <div class="title border-topbottom">{{key}}</div>
        <div
          class="item-list"
          v-for="innerItem of item"
          :key="innerItem.id"
          @click='handleCityClick(innerItem.name)'
        >
          <div class="item border-bottom">{{innerItem.name}}</div>
				</div> 
			</div>
			</div>
		</div>
</template>	

<script>
import Bscroll from 'better-scroll'
export default {
	name:'CityList',
	props:{
    	hotCities: Array,
    	cities: Object,
    	letter:String
	},
	methods:{
		handleCityClick (city){
			this.$store.dispatch('changeCity',city)
			 this.$router.push('/')
		}
	},
  	mounted () {
    	this.scroll = new Bscroll(this.$refs.wrapper)
	  },
	  watch: {
	    letter () {
	      if (this.letter) {
	        const element = this.$refs[this.letter][0]
	        this.scroll.scrollToElement(element)
	  }
  	}
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
	.border-topbottom
		&:before
			border-color:#ccc
		&:after
			border-color:#ccc
	.border-bottom
		&:before
			border-color:#ccc
	.list
		position:absolute
		overflow:hidden
		top: 1.58rem
		left:0	
		right:0
		bottom:0		
		.title
			line-height:.54rem
			background: #eee
			padding-left:.2rem
			color:#666
			font-size:.26rem
		.button-list
			overflow:hidden
			padding:.1rem
			padding:.1rem .6rem .1rem  .1rem
			.button-wraper
				width: 33.33%
				float:left
				.button	
					text-align:center
					padding:.1rem 0
					margin: .1rem
					border:.02rem solid #ccc
					border-radius:.1rem
				.button-bg
					background: #FF69B4
					color:#fff
		.item-list
			.item
				line-height:.76rem
				color:#666
				padding-left:.2rem
		
</style>