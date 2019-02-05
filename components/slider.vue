<template lang="pug">
	.slider
		h3.slider__headline Уровень владения JavaScript
		.slider__wrapper
			.slider__arrow( v-bind:style="{ left: left + '%'}" )
				.slider__arrow-img 
			.slider__line
			.slider__points
				span.slider__points-point
				span.slider__points-point
				span.slider__points-point
				span.slider__points-point
			.slider__text
				p.slider__text-level( v-on:click="left = -0.8") Не владею
				p.slider__text-level( v-on:click="left = 17.4") Использую готовые решения
				p.slider__text-level( v-on:click="left = 49.1") Использую готовые решения и умею их переделывать
				p.slider__text-level( v-on:click="left = 98.7") Пишу сложный JS с нуля

</template>


<script>
export default {
	data(){
		return{
			left: 49.1
		}
	}
}

</script>

<style lang="scss">
.slider{
	position: relative;

	width: 100%;
	padding-bottom: 40px;

	&__headline{
		width: 100%;
		margin: 0;
		margin-bottom: 37px;

		font-size: 23px;
		font-weight: 700;
		color: #2f1b15;
		line-height: 1;
	}

	&__wrapper{
		position: relative;

		width: 100%;
	}

	&__arrow{
		position: absolute;
		top: -16px;

		width: 17px;
		height: 14px;

		transition: left .3s cubic-bezier(.15,.46,.48,1.13);

		&-img{
			width: 17px;
			height: 14px;

			background-image: url("../assets/arrow.png");
		}
	}

	&__line{
		width: 100%;
		height: 4px;
		margin-top: 4px;

		background-image: url("../assets/line.png");
		background-position: 0 100%;
		background-size: cover;
		background-repeat: repeat-x;
	}

	&__points{
		position: relative;

		display: flex;
		width: 100%;
		margin-bottom: 25px;

		&-point{
			position: absolute;
			top: 0;

			width: 3px;
			height: 12px;
			margin-top: -2px;

			background-color: #3f241e;

			&:nth-child(1){
				left: 0;
				height: 20px;
			}

			&:nth-child(2){
				left: 18.2%;
			}

			&:nth-child(3){
				left: 50%;
			}
			
			&:nth-child(4){
				right: 0;
				height: 20px;
			}
		}
	}

	&__text{
		position: relative;

		display: flex;
		justify-content: space-between;
		width: 100%;

		&-level{
			position: relative;

			margin: 0;

			font-size: 13px;
			font-weight: 700;
			color: #3f241e;

			cursor: pointer;

			&:nth-child(3){
				width: 22%;
			}
		}
	}
}








</style>