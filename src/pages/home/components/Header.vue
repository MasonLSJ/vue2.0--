<template>
	<div class="header">
		<div class="header-left ">
			<div class="iconfont back-icon">&#xe624;</div>
		</div>
		<div class="header-input">
		<span class="iconfont">&#xe632;</span> 请输入你想去嗨皮的地方</div>
		<div class="header-right">
			城市
			<span class="iconfont arrow-icon">&#xe64a;</span>
		</div>
	</div>
</template>

<script>
export default {
	name:'HomeHeader'
}
</script>

<style lang="stylus" scoped>
 @import "~styles/varibles.styl"
	.header
		display:flex
		height: .86rem
		background: $bgColor
		color:#fff
		line-height:.86rem
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
			width: 1.24rem
			float:right
			text-align:center
			.arrow-icon
				font-size:.24rem
</style>