<template>
	<div class="header">
		<div class="header-left ">
			<div class="iconfont back-icon">&#xe624;</div>
		</div>
		<div class="header-input">
		<span class="iconfont">&#xe632;</span> 请输入你想去嗨皮的地方</div>
		<router-link to='/city'>
			<div class="header-right">
				{{this.$store.state.city}}
				<span class="iconfont arrow-icon">&#xe64a;</span>
			</div>
		</router-link>
	</div>
</template>

<script>
export default {
	name:'HomeHeader',
	props:{
		city:String
	}
}
</script>

<style lang="stylus" scoped>
 @import "~styles/varibles.styl"
	.header
		display:flex
		height: $headerHeight
		background: $bgColor
		color:#fff
		line-height:$headerHeight
		.header-left
			width: .64rem
			float: left
			text-align:center
			.back-icon
				text-aligin:center
				font-size:.4rem			
		.header-input
			flex:1
			margin-top: .12rem
			margin-bottom: .12rem
			margin-left: .2rem
			line-height:.62rem
			padding-left:.2rem
			background: #fff
			border-radius:.1rem
			color:#ccc
		.header-right
			min-width: 1.04rem
			padding:0 .1rem
			float:right
			text-align:center
			color:#fff
			.arrow-icon
				font-size:.24rem
</style>