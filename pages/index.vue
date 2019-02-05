<template lang="pug">
	.container
		.secret
			img.secret__img(src="../assets/secret.png" alt="image top secret")
		.wrapper
			.case
				img.case__img(src="../assets/case.png" alt="image case")
			info
			checkbox
			slider
			about
			future
			date

</template>

<script>
import Info from '~/components/info_block.vue';
import Checkbox from '~/components/checkbox.vue';
import Slider from '~/components/slider.vue';
import About from '~/components/about.vue';
import Future from '~/components/future.vue';
import Date from '~/components/date.vue';

export default {
	name: "index",

	components: {
		Info,
		Checkbox,
		Slider,
		About,
		Future,
		Date
	}
}
</script>

<style lang='scss'>

*{
	box-sizing: border-box;

	&:before, &:after{
		box-sizing: border-box;
	}
}

body{
	width: 100%;
	height: auto;

	background-color: #797979;

	font-family: 'PT Sans', sans-serif;
}

.container{
	position: relative;

	width: 1000px;
	height: 100%;
	margin: 0 auto;

	background-image: url(../assets/background.jpg);
}

.secret{
	position: relative;

	display: flex;
	justify-content: flex-end;
	align-items: flex-end;
	width: 100%;
	height: 150px;

	&__img{
		margin-right: 55px;
	}
}

.wrapper{
	position: relative;

	width: 100%;
	padding: 0 115px;
}

.case{
	position: relative;
	
	display: flex;
	justify-content: center;
	align-items: center;
	width: 100%;
	margin-bottom: 60px;
}

</style>

